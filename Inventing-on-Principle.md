# Reference
https://www.youtube.com/watch?v=EGqwXt90ZqA&t=576s

Guiding principle
Instead of just following your passion or doing something you love, following a guiding principle that guides us time to time for long term

Ideas
1. bringing ideas into the world is one of the most important things that people do 
2. great ideas in the form of great art stories inventions scientific theories give meaning to our lives as people ponder about how ideas grow
3. Immediate connection (Tools should create healthy environment to become creative)
	1. provide quick feedback loops(thinking->see in action -> build on top of it) opens up possibility to try many ideas as soon as you think of them and it is very important for creative thinking.
	2. If any delay in feedback loop, whole world of ideas will never lead to fruition - thoughts we can't think.
	3. Ideas at start are tiny, weak and fragile, creator need to nurture, develop and mature and need an environment to shape their growth
	4. show the data, show the comparisons

 fragile in order to develop and mature
ideas need an environment or the creator can nurture them we kind of take care of
them feed them and shape their growth and to me that's what this principle of media connection is all about and
because ideas are so precious to me when I see this principle violated but I see
ideas stillborn or stunted because the Creator can see what they're doing I feel that's wrong and not wrong in the
sense of violating some UI guideline or going against some best practice but wrong in a deeper sense than that and
I'll come back to this but I want to show you another example of following this principle so in this code here there's no state there's no present
state so there's no time there's no interactivity and I was thinking about how would we handle those aspects of
coding in a way that's in line with this principle I have creators need an immediate connection so what I have here
is a little platformer game so here's my little guy can run around he can jump
you can die and the code for M is over here so this
code makes them run around this makes them chomp just makes them collide with things and down here I've got some code
for this little turtle and the turtle is not doing much right now because I haven't finished writing his code so I'm
just going to do that right now say on each tick his exposition plus equals his Direction times the time interval 1 6 2
for the second time some speed which no no could be fast could be slow it's
negative he walks backwards and these are all ideas I can use for
other enemies but I think turtles are supposed to be slow so that's a good
speed for a turtle and then up here I've got some code that says when my guy
collides with the turtle he gets some Y velocity so he bounces into the air and the turtle gets stomped so that looks
like that and like Charlie gets up at for a bit the problem is I don't want
the player to be able to get up here yet I want the player to bounce off the turtle and go through this little
passageway down here and I'll have to go around and you know solve puzzles and whatnot come back and get the star so
the turtle is too bouncy right now now of course I can just turn that down in the code and now I can try it but now
it's not bouncing enough and so well it's nice that I can adjust the code while it's running
Steff having to stop and recompile and find my place again I can't immediately see what I need to
see which is whether or not he can make that jump so here's what I'm gonna do
I'm going to bounce off the turtle and pause the game so I pause the game and
now there's the slider up here which lets me rewind through time
and now I could rewind to back before I made the jump and change the code make
them less bouncy and now when I move it forward it's going to simulate forward using the same input controls the same
keyboard commands that record us before but the new code this is not good enough
I need to be able to see changes
immediately I need to be able to see immediately whether or not my bounciness is correct
none of this stuff and if you have a process of time and you want to see
changes immediately you have to map time to space so here's what I'm gonna do
there bounce off my turtle pause the game and now hit this button here which
shows my guys trail so now I can see where he's been and when I rewind this
trail in front of him is where he's going to be this is his future and when
I changed the code I change his future so I can find exactly the value I need
so when I hit play he slips right in there
so creators need to be able to see what they're doing if you're designing something embedded in time you need to
be able to control time you need to be able to see across time otherwise they're deciding blind as I was playing
with this I know it's fun to play with gravity so I can make gravity a little negative and he starts to float up in
the air and I can kind of play with that and try to get them to try to stay there and you
could probably make an entire game around just just mechanic hair it's gravity manipulation in fact I bet I could
fiddle with any part of this code and come up with an idea for a game even if I just if I just comment out the first
statement in the code now Mike I can't move left you could only move right
which sounds kind of silly but Terry Cavanagh actually made a beautiful game around that concept called don't look
back terry cavanagh he made another really
wonderful game but you might have seen called V billed as letter V six times and the way that game works is that you
can't jump instead you can only flip a play down and you fall up instead of
falling down so it kind of works like this that you'd phone on the ceiling or you can walk around on the ground and so
you'd have these levels which kind of look like this and you'd kind of walk
around you have to learn how to navigate terrain like this and so if you had like
something like that you won't be able to jump over you'd have to like flip over and flip over and you got an amazing amount of gameplay about out of this
concept so again being able to try ideas as you think of them
this example in the last moment the tree these are both very visual programs
we're able to see our changes just by seeing how the picture changes so I was thinking about how we could do more
abstract coding that's more in line with this principle how can we write a generic algorithm in such a way that we
can see what we're doing so as an example let's take a look at binary search super quick refresher on how
binary search works you have an array of values that are in order and you have a key which is value that you're trying to
locate within the array and you keep track of two variables which are the lower and upper bounds of where you
think that value could possibly be right now it could be anywhere and you look right in the middle of that range what
you find is too small then he has to be after that look in the middle of a range what you find is too big he has to be
before that and you kind of keep subdividing your range until you narrow in on value you're looking for and in
code binary search looks like this and from my perspective you can't see
Binary search
anything here you can't see anything I see the word array but I don't actually see an array and so in order to write
code like this you have to imagine an array in your head and you essentially have to play computer you have to
simulate in your head what each line of code would do on a computer and to a
large extent the people that we consider these skilled software engineers are just those people that are really good at playing computer but for writing our
code on a computer why are we simulating what a computer would do in our head why
isn't the computer doesn't do it and show us so let's write binary search function
binary search takes a key and an array and then over here on this side it's
saying okay it takes key in an array such as what give me an example need
something to work with here so first since my array might be a b c d
e f and let's say for instance we're looking for the d so now let's start
coding the lower balance starts out at 0 over here says lo equals 0 nothing
amazing there upper bound starts out at the end of the array so high equals
array length minus 1 and over here it says high equals 5 so I have my Abstract
formula and the code over here it's give me the concrete value corresponding to
these example arguments so I don't have to maintain this picture in my head it's
just showing it to me so now I need the the index in the middle of the array so
I'm going to take the average of those two mid equals lo plus high over 2 and
well that's obviously an all right 2.5 is not a valid array X so I guess I need
to round this off so I'm going to add the floor function and around it down to 2 and I caught that book literally the
second I typed it instead of writing the entire function and 20 unit tests so now
I get the value out of the array and then I need to subdivide my range which
so there's an if statement which I'll just paste in here so in this case the
the value I found is less than the key so it's taking this first branch of the if statements this is adjusting the
lower bound of course the key was smaller then it would take the spread of
the if statement and adjust the upper bound or if the key was C then we would
have just happened to find it on the first shot and we'd return the index so this is the first iteration of this
algorithm and now what we need to do is loop we've subdivided the array we need
to keep subdividing until we narrow in on what we're looking for so each a loop I will just loop while
one do all this and now what we have are
three columns corresponding to three iterations of this loop so this first
column here is exactly what you saw before low and high span the entire array we found a C it was too low so we have just
our lower bound loop up to here second iteration bounds are tighter we found an e at just the upper bound third
iteration loop up here low and higher the same we've never do count to a single candidate is indeed the key we're
looking for and we return its index so there's nothing hidden here you see
exactly what the algorithm is doing at every point and I can go up to here try different keys so I can see how the
algorithm behaves for these different input arguments and by looking across the Stata I can develop an intuition for
how this algorithm works so I'm trying different keys here and say I tried looking for a G and this
looks a little different it's not actually returning and the reason for
this is I'm looking for a key which is not actually in the array and the only way of breaking out of this loop is by
finding the key so it's kind of stuck here looping forever so we can take a
look at this and see what went wrong where's this algorithm going off the rails these first few iterations look
fine but this this iteration looks weird because lo is greater than high where
our range is completely collapsed so if we get to this point then we know the key can't be found so I see this faulty
condition here I say oh that's not right lo has to be less than or equal to high okay well I'll just put that over as the
condition of my well statement low less than equal to high and then that would break out of the loop and I would return
some Sentinel to say that could be found so here we have three iterations the loop going to be found we return the not
valid value so that's what it might be like to write an algorithm without a blindfold on
so I've got this principle again that creators need to be able to see what
they're doing the fit need this media connection what they're making and I've tried to show this principle through three coding examples but that's just
because this is a software engineering conference I thought I was supposed to talk about programming but to me this
principle has nothing to do with programming particular it has to do with
any type of creation so I'd like to show you a couple more demos just to show you the breadth of what I have in mind here
so to begin with let's take a look at different branch of engineering so here
Circuit design
have an electronic circuit that I drew I'm not quite done drawing it so let me finish up there and now we have a
working circuit I mean I assume it's a working circuit I don't actually see
anything working here so this is exactly the same as writing code that we work in
the static representation but what we actually care about is the data the values of the variable so we can't see
that here now in a circuit the variables are the voltages on these different
wires so each of these wires has a voltage that's changing over time and we have to be able to see that now if I was
building this circuit on a lab bench building it physically I could at least take an oscilloscope and kind of poke
around and see what's going on the different wires what's going on here or here so at the very least I should be
able to do that so what I have here is a plot of the voltage on this wire over
time we can see it's high it's low high and low so this is clearly oscillating
if I built this physically also I would actually be able to see the circuit doing something so in this case I've got
these two LEDs up here these are LEDs the lights presumably they're there for
a reason I can hit play and watch it simulate out in real time so now you can see what the
circuits doing
in order to design a circuit like this you have to understand the voltage on every wire you have to understand how
all the voltages are changing throughout the entire circuit and just like coding either environment shows that to you or
you simulate it in your head and I have better things do with my head then simulate what electrons are doing so
what I'm going to do I'm gonna spread these out a little bit so the same circuit just spread out a little bit and
I'm going to add the voltage at every node so now you can see every voltage
throughout the circuit and I can even hit play and watch it all kind of simulate out in real time although what
I prefer to do is just move my mouse over it and I can kind of look in areas
that are interesting to me and see what the values are I can compare any two nodes so if you look at say the node
over here while I mouse over this one you see the shadow of the one I'm messing over is overlaid on that the
shadow of the one on masking over is actually overlaid on all of them and so I can compare any two nodes just by
mousing over one of them and looking at the other one and again I can
immediately see results of my changes so I've got the 70k resistor here I want to
change its value I just click and drag it and now I see the waveforms changing immediately and you'll notice that when
I click and drag it leaves behind the shadow of the waveform before I started dragging so I can compare I can
immediately see the results of my changes to golden rules of information
design show the data show comparisons that's all I'm doing here but even this
isn't quite good enough what we're seeing here are the voltages but in electronics there's actually two data
type so it's voltage and there's current what we're not seeing is the current flowing through each of these components
and order to design a circuit you need to understand both the voltage and the current you need to understand the interplay between the two
that's what analog design is so what I'm going to do is spread these out a little bit more and now I'm going to replace
each of these components with a plot of the current going through it over time so each of these blue boxes
represents a component and you can see which component it is because as a little badge in the corner a little icon
but now you can see everything that's going on in circuit you see how the
current changes you can see how voltage and the current changes there's nothing
hidden there's nothing to simulate in your head so what we have here is a
different way of representing a circuit just in general you could draw any
circuit with these blocks but instead of being made out of little squiggly symbols it's made out of data and I
think it's important to ask why do we have these squiggly symbols in the first place why do they exist they exist
because they're easy to draw with pencil on paper this is not paper so when you
have a new medium you have to rethink these things you have to think how can this new medium allow us more media
connection to what we're making how can this new medium allow us to work in such a way we can see what we're doing it's
really the same situation with programming our current conception of what a computer program is a list of
textual definitions that you hand to a compiler that's derived straight from Fortran Algol late 50s those languages
were designed for punch cards so you would type your program onto a stack of cards and hand it to the computer
Interactive programming
operator it's the guy in the bottom picture and you would come back later so there was no such thing as interactivity
back then and that assumption is baked into our current notions of what programming is C was designed for
teletypes so that's Ken Thompson and Dennis Ritchie up there Ritchie made C
and there are no video displays in this picture Ritchie is basically typing on a
fancy typewriter that types back to him any time you use a console or terminal
window you're emulating a teletype and even today people still think of a
ripple or an interactive top level as being interactive programming because that's the best that you could do on a
teletype so I have one more demo I'll show
because I want emphasize that this principle media connection is not even
about engineering it's about any type information so I want to move to a different field entirely so let's think
about animation so I've got this painting here with the tree and leaf on
Traditional animation
it and I want to make a little video with the leaf kind of drifting down in
the tree and the normal way of doing this in a conventional animation package like flash is through keyframes so you
basically say where you want the leaf to be at different points of time and then you hit play and see what it looks like
so I'm gonna say okay at frame 20 I'm
gonna create a keyframe and leaf should be there at frame 40 pretty keyframe and
leave for me there and I am just totally guessing here I cannot see the motion I cannot feel the timing I'm just throwing
things in time and space so I've got
this leaf at different points of time I'm going to add a tween which tells flash to connect the dots and then I'm
going to hit play and see what it looks like and it looks ridiculous it looks
like billiard balls bouncing back and forth and the thing is I kind of know
what I want right it's a leaf I want Leafs drifting down from a tree and I
can even kind of perform that see with my hand leave drifting down from a tree the flash doesn't know how to listen to
my hand but maybe there's a new medium that doesn't know something about
listening to my hand so what I'm going to show you here is a little app I made
for performing animation and we're not really set up to do live demo off the
iPad so I'm just gonna play you a video of me making a video
the way the scene is gonna play out is the leaf is gonna kind of drift down the tree and it seems gonna pan over and the
rapids gonna do something and two things one this is gonna move pretty quickly
Using both hands
and second I'm gonna be using both hands at almost all times so I've got these
different layers the background the ground the foreground I'm choosing which letter to move using a left thumb I'm gonna move my leaf to its position move
my bunny offstage and start time rolling and now I'm going to perform the leaf
drifting down from the tree run it back check out that how that
looked the motion looks pretty good but the leaf kind of needs to rock back and forth so I'm gonna pull out a rotation
controller run it back find where the lease is about to break off and record
the rotation and I had a little flip there just because they felt right in the moment it wasn't even planned stop
because I want to pan over so I want to drag a whole bunch of layers at once I grab all the layers into the list I turn down the sensitivity of the background
layers so they'll move slower for a kind of parallax effect I only want to move horizontally so I pull out a horizontal
tracker and check out how it looks I don't quite like the parallax so I just
infuse a little bit try out again I like that better so I get ready to go I run it back to
the beginning so I can kind of get back into the rhythm of the piece the leaf
hits I wait a beat and I start panning and I don't know how many frames I
waited I don't know how long it was I went when it felt right so I pan over to
this winter scene and kind of slowed down stop and then I run it back because I'm gonna do some flying bunny throw
away this tools comes I'm done with them and wait until I think my bunny should
move and he hops away and I've got a few different poses from a bunny so I pull
those out and then I find the point where the bunny is about to take off the ground
which is right there I switch his pose and I kind of toggle between the poses as he hops away and then I run it back
because I want to check out how it looked and I'm just going to bring that up full screen for you this is a piece
The Leaf
you
so I made that in two minutes performing with my hands like a musical instrument very immediate connection between me and
what I was trying to make
one of the inspirations for this tool was an animation that I tried to make several years ago not that one but it
also began with the Leafs drifting down from a tree and I spent all day in flash trying to keyframe that leaf could do it
and so that was the end of that you know I I still have my storyboards sometimes
I play the music I wrote for the piece but the piece itself is locked in my head and so I always think about the
millions of pieces are locked in billions of heads in not just animation
and not just art but all kinds of ideas all kinds of ideas including critically
important ideas world-changing inventions life-saving scientific discoveries these are all ideas that
must be grown and without an environment in which they can grow or their Creator
can nurture them with this immediate connection many of these ideas will not emerge or Thole emerge stunted so I have
this principle that creators need an immediate connection and all those demos that I just showed you simply came from
The Guiding Principle
me looking around noticing places where that principle was violated and then
trying to fix that that's really all I did I just followed this guiding
principle and it guided me to what I had to do
but I haven't said much about the most important part of the story which is why why I have this principle why I do this
Responsibility
when I see a violation of this principle I don't think of that as an opportunity
when I see creators constrained by their tools their ideas compromised I don't
say oh good an opportunity to make a product an opportunity to start a business or an opportunity to do
research or contribute to a field I'm not excited by finding a problem to solve I'm not in this for the joy of
making things ideas are very precious to me and when I see ideas dying it hurts I
see a tragedy to me it feels like a moral wrong it feels like an injustice
and if I think there's anything I can do about it I feel it's my responsibility to do so not opportunity but
responsibility now this is just my thing I'm not asking you to believe in this the way that I do my point here is that
these words that I'm using in justice responsibility moral wrong these aren't
the words we normally hear in technical field we do hear these words in
association with social causes so things like censorship gender discrimination
environmental destruction we all recognize these things as moral wrongs
most of us wouldn't witness a civil rights violation think a good an opportunity I hope not instead we've
been very fortunate to have had people throughout history who recognized these social wrongs and saw it as the
responsibility to address them and so there's this activist lifestyle where a person dedicates themselves to fighting
for a cause that they believe in and the purpose of this talk is to tell you that
this activist lifestyle is not just for social activism as a technologist you
can recognize the wrong in the world you can a vision for what a better world could be and you can dedicate yourself to
fighting for principle social activists typically fight by organizing but you can fight by
inventing so now I'd like to tell you
Larry Tesler
about a few other people who have lived this way starting with Larry Tesler Larry has
done a lot of wonderful things in his life but the work I'm gonna tell you about he did in the mid 70s at Xerox
PARC and at the time it really wasn't a such thing as personal computers the
notion of person computing was very young and Larry and his colleagues at Parc felt that it had transformative
potential that personal computing could change how people thought and lived and
I think all of us in this room would agree that they should not be right about that but at the time software
interfaces were designed around modes so in a text editor for instance you
couldn't just type and have words appear on the screen like on typewriter you would be in command mode if you wanted
to insert text you'd have to press I to go into insert mode and escape back out to command mode or maybe you hit a to go
into ependymoma want to move text around you hit em to go into move mode and they'd have to select and you being mode to select and move things around and
Larry would watch people using the computer Larry actually pioneered the
concept of software user studies another thing that he did but he would watch people using software and he found that
many people even after training and weeks of use many people were not becoming comfortable with the computer
and he believed that it was these modes that were to blame him that the the
complexity of modes was a kind of barrier that many people couldn't get across and so this kind of represented a
threat to this dream of what personal computing be so Larry made it his
personal mission to eliminate modes from software and he formed a principle no person should be trapped in a mode his
slogan that he would go around saying was don't Mode me in and he had it printed on a t-shirt and this principle
informed everything that he did he he thought about it with all the work that you did and eventually he came up
with a text editor called gypsy which essentially introduced text editing as we know today there was an
insertion point and when you typed words appeared on the screen to select text he
invented most less selections with click and drag so you just click and drag over the text you want to select like he was
using a highlighter one of the first uses of drag to move text around he
invented these commands that he called cut copy paste every select and cut later on you pasted in whenever you're
ready you've never trapped in a mode after switching between modes when you hit the W key on the keyboard you get W on the
screen always and he would watch people using his software and he found that
someone who had never seen a computer before which was most people back then could be up and running like half-hour
so this was clearly a transformative change in enabling people to connect with computers and his ideas about mote
lessness spread to the rest of the desktop interface which was then being invented a park at the same time and
today they're so ingrained in the computing experience that we kind of take them for granted now I said that
Larry made illumination of modes his personal mission that's actually his
words and if you think he's exaggerating here's Larry's license plate for the last 30 years
What did Larry do
nowadays of course Larry has a website at know modes comm and he is on Twitter
it's no modes and so like I said Larry has done a lot of amazing work in his
career but his self-identity is clearly associated with this cause and so I'd
like to ask what what exactly did Larry do like how would we best describe what
Larry did the typical biography might say Larry Tesler invented cut copy paste
which is true but I think that's really misleading because this invention was
very different than say Thomas Edison inventing the phonograph Edison basically just stumbled over the
technology for audio recording and he built it as novelty and yeah he came up with like a list of possible
applications for this technology but he didn't have any cultural intent whereas
what Larry did was entirely a reaction to a particular cultural context so
another thing that you might hear is that Larry Tesler solved the problem of modeless text manipulation solved the
problem and you know obviously that's true he worked on this problem for a long time eventually solved it but I
think that's really misleading too because this problem that he solved only
existed in his own head nobody else saw this as a problem for everybody else
modes were just how computers worked it wasn't anything wrong with them any more than we think there's something wrong
with having two arms it's just that was a fact of life so the first thing that
Larry did was that he recognized or wrong that had been unacknowledged in the culture and the thing is that's how
many great social changes began as well so 150 years ago Elizabeth Cady Stanton
Elizabeth Cady Stanton
had to stand up and say women should vote in everybody else sadly that's crazy what are you talking about today
we recognize gender discrimination is wrong back then it was part of society
whose invisible she had to recognize it and she had to fight it and to me that's a much closer
model to what Larry did when the Thomas Edison model of inventing a bunch of random technologies hukum patented now
to be clear I'm not making the judgments about the relative importance or impact of these two people I'm just talking about their motivations and their
approach both of them recognize a cultural wrong they envisioned a world
without that wrong and they dedicated himself to fighting for a principle she
fought by organizing he fought by inventing and many other seminal figures
in computing had similar motivations so certainly Doug Engelbart Doug
Doug Engelbart
Engelbart basically invented interactive computing the concept of putting
information on a screen navigating through it looking at information in different ways pointing to things and
manipulating them he came up with all this at a time when real time interaction with the computer was just almost unheard of today he's best known
as the inventor of the mouse but what he really invented was this entirely new way of working knowledge his explicit
goal from the beginning was to enable mankind to solve the world's urgent problems and his vision he had this
vision of what he called knowledge workers using complex powerful information tools to harness their
collective intelligence and he only got into computers because he had a hunch that these newfangled computer things
could help him realize that vision everything that he did was almost single
mindedly driven by pursuing this vision here's Alan Kay Alan Kay ran the lab at
Alan Kay
Starks Park where we got the desktop interface so things like windows and icons command menus he also invented
object-oriented programming lots of other things his goal and I quote was to
amplify human reach and bring new ways of thinking to a faltering civilization that desperately needed it is that great
his approach was through children he believed that if children became fluent
in thinking in the medium of the computer meaning if if programming was a
form of look basic literacy like reading and writing then they become adults with new forms of critical thought new ways of
understanding the world and we'd have this more enlightened society similar to the similar to the the difference that
literacy brought to society and everything they did everything he invented came out of pursuing this this
vision this goal with children and following principles that he adopted
from PJ and Montessori Jerome Bruner these people who had studied how children think and the figure probably
most widely associated with software activism is Richard Stallman Stoll men
Richard Stallman
started the canoe project which today makes up a big chunk of any Linux system he also started the free software
foundation wrote GCC GPL many many other things his principle is that software
must be free as in freedom and he has very precise meaning associated that statement he's always been very clear
that software freedoms and that of moral right and wrong and he's taken a particularly uncompromising approach in
his own life to that all of these tremendously influential people
dedicated their lives to fighting for a particular ideal with a very clear sense
of right and wrong often really fighting against an authority or mainstream that
did not recognize the wrong as being wrong and today the world is still very far from any of their ideals and so they
still see a world in crisis and they keep fighting they're always fighting
now I'm not saying that you have to live this way I'm not saying that you should
live this way what I'm saying is that you can if this lifestyle is an option
that's available to you and it's not when they're going to hear about much your career counselors not gonna come back to you and say you should start a
personal crusade in a social field they might but not in technology instead the
world will try to make you define yourself by a skill that's why you have
a major in college that's why you have a job title you are a software engineer and you'll probably specialize to be a
database engineer or front-end engineer you'll be given front-end and asked to engineer them and that can be worthwhile
and valuable and if you want to spend your life pursuing excellence in
practicing a skill you can do that that is the path of the craftsman that is the
most common path it's the only other path you really hear about much is the path of the problem-solver so I see
entrepreneurship and academic research as kind of two sites that coin there's a field there's a set of problems in that
field or NEETs in the market you go in you choose one you work it you make your contribution there maybe later on you
choose another problem you work it make your contribution there again that can be worthwhile valuable and if that's
what you want to do then you can take that path but I don't see Larry Tesler on either of those paths I wouldn't say
that he was contributing to the field of user experience design because there was no such thing he didn't choose some open
problem to solve he came up some problem would only existed in his own head and no one else even recognized and
certainly he did not define himself by his craft he defined himself by his cause by the principle he fought to
upheld I'm sure if you look at Wikipedia it will say that he's a computer
scientist or user experience something but to me that's like singles with Cady
Stanton was a community organizer no Elizabeth Cady Stanton established the
principle of women's suffrage that's who she was that was the identity she chose and Larry Tesler established the prints
most lessness he had this vision he brought the world to that vision so you
Finding a Principle
can choose this life or maybe it will end up choosing you it might not happen right away it can take time to find a
principle because finding a principle is essentially a form of self-discovery that you're trying to figure out what
your life is supposed to be about what you want to stand for as a person it took me like a decade ten years
before any real understanding of my principles solidified that was my 20s when I was young I I felt I had to live
this way but I would get little glimmers of what mattered to me but no big
picture it was really unclear and this was very distressing for me what I had
to do was just do a lot of things make many things make many types of things
study many things experience many many things and use all these experiences as
ways of analyzing myself taking all these experiences and saying does this resonate with me does this propel me do
I not care building up this corpus of experiences that I felt very strongly about for some reason and trying to make
sense of it trying to figure out why what is the secret ingredient all these experiences than reacting to so strongly
now I think everyone's different and all those guys I talked about they have their own origin stories which you can
read about I will just say that confining yourself to practicing a
single skill can make it difficult to get that broad range of experience which seems to be so valuable for the sort of
work and finally if you choose to follow
Following a Principle
a principle the principle can't just be any old thing you believe in you'll hear
a lot of people say that they want to make software easier to use or they want to delight their users or they want to
make things simple that's a really big one right now everyone wants to make things simple and those are nice thoughts they maybe give you a little
kind of give you a direction to go in but they're too vague to be directly actionable Larry Tesler likes simplicity
but principal was the specific nugget of insight no person should be trapped in a
mode and that is a powerful principle because it gave him a new way of seeing
the world it defied the world's our right and wrong in a fairly objective way so he could look at somebody
selecting text and ask is this person in a mode yes or no if yes yet to do
something about that and likewise I believe that creators need powerful tools it's a nice thought that doesn't
really get me anywhere my principle is that creators need this a media connection so I can watch you changing a
line of code and I can ask did you immediately see the effect of that change yes or no if no I got to do
something about that and again all those demos that I showed you came out of me
doing that of me following this principle and letting it lead me to exactly what I need to do so if your
guiding principle embodies the specific insight it will guide you and you'll
always know if what you're doing is right
there are many ways to live your life that's maybe the most important thing you can realize in your life is that
every aspect of your life is a choice with our default choices you can choose
to sleepwalk through your life and accept the past that's been laid out for you you can choose to accept the world
as it is but you don't have to if
there's something in the world you feel the wrong and you have a vision for what a better world could be you can find
your guiding principle and you can fight for a cause so after this talk I'd like
you to take a little time and think about what matters to you what you believe in and what you might fight for
thank you
you
