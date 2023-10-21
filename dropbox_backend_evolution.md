# References
https://www.youtube.com/watch?v=PE4gwstWhmc

# Core Theme
how dropbox dealt with the technical backend challenges with very minimal resources 

# Constraints
1. Infra challenge - startup of 2 engineers, not having google like infra to build on top of it.
2. Time challenge - don’t have time to invest 5 years to build something like bigtable, gfs etc.
3. Tech Stack selection challenge - fast-changing back end tech stack ecosystem, a very quickly growing environment where your resources are growing at the same time as the demands

# Functional requirements
1. Upload
2. Download
3. deduplication support - when two users uploading same file

# NFR
1. support large scale of clients and data
2. Client should use limited user device resources and bandwidth
3. very high scale of writes 
4. In case of data available offline - Dropbox clients store complete copy of user data
5. Dropbox client can cache recently used data
6. Metadata Db side sharding challenge:
    1. Let say we have user based sharing but users and shared folder relationships cut across different users are difficult to shard.
    2. Also introducing sharding a later stage is difficult in terms of existing code migration
7. ACID requirements
        3. Atomicity - complete file not visible post successful upload
        4. consistency(no data mismatch)
            1. Share a folder excluding one file which you mark for deletion but post sharing the folder you find - users were able to access the deleted file.
        5. Durability -  no data loss

# Architecture evolve Journey & Milestones

## V1 - Early stage 3 member team early stages backend choices made
1. Store data on **local disks** with mysql for metadata
2. Challenges faced
    2. Disk space overflows
    3. Server overloaded
       
## V2
1. S3 for user data storage with separate servers hosting mysql for metadata
2. Challenges faced 
    1. Server overload in handling different features - download and upload functionality was heavy and it started affecting other features like user mgmt., syncing, client’s notifications etc.

## V3 - 50k user base
1. Separate metadata, block upload and notif  microservices
2. Block service talks to metadata service for metadata updates over api hits
3. Added **caching memcach**e to delay/postpone db side sharding/partitioning for later
4. Notif service cluster with each maintaining around million of connections
5. Horizontally scale metaservers and block servers
6. Challenges
    1. **Db side scaling** - sharing, partitioning
    2. **Memcache lib was modified for strong consistency requirements.**
    3. Too many users doing polling to notif servers was a bottleneck
    4. Python GIL and load balancer cluster gotchas
    5. Easier to do from scratch than migrating a non sharded database to sharded architecture complexity 
        1.  transaction flow has to be revisited considering distributed db nodes in action.
        2. **distributed joins**
    6. Very high throughput notification server - millions of connected clients at any point of time
