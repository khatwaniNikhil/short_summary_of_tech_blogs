# References
https://zerodha.tech/blog/logging-at-zerodha/

# Summary
## Why ELK wasn’t the right fit for us
1. Slower ingestion times into Elasticsearch (Logstash pipeline slowdown)
2. Storage costs skyrocketed as each incoming field is indexed for searching(3-4x of original size, also retain logs - multiple years)
3. UX for search using lucene or KQL subpar
4. Elasticsearch is slow for aggregate queries over a long period
5. RBAC was missing

## Alternatives
1. Grafana Loki
2. cLoki and Clickhouse
3. Zerodha's loj (Vector + Clickhouse + Metabase)

## Why loj
1. Clickhouse is an excellent fit for logging
	1. column oriented well suited for OLAP and logging data (read-heavy, large batch bulk inserts but no later mutations)
	2. compression reduce the amount of data during read flow
	3. easy to scale and setup cluster
	4. schema for storing data:
		application logs already had well defined schema
		created specific schema for exceptional cases(SMTP logs and AWS Pinpoint logs).
		custom HTTP Log schema that contains standard HTTP access log fields for storing logs from various proxies like NGINX/HAProxy 
		phenomenal 5X reduction in the size of the same set of logs.
	5. cloudfare case study
			https://blog.cloudflare.com/http-analytics-for-6m-requests-per-second-using-clickhouse/
		
2. Why Metabase
	robust RBAC system to ensure that each team member can only access the data they are authorized to view. 
	ability to pre-format query templates for non-technical teams need

	cons
	live tailing of logs missing
	performing context-specific queries can be difficult.
	lack of a user interface to slice and drill logs based on time periods.

3. Why vector
	ultra-fast log shipping agent that has a low resource overhead





	

