# No computer project

_Note: I'm writing this from the perspective of the designers of the real-world DSL Lego._ 

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Think of the children. There are so many kids in the world without an outlet for their creativity. This language will serve future artists and engineers who want a way to express themselves in the physical world. The concept is simple: design a small (but extendable) set of multicolored bricks with attachments that allow you to connect them to other bricks. Kids can then compose these bricks to make sculptures, models, impressionistic art, whatever they want! In fact, they'll get so attached to their projects that it will be really difficult to break them down so that their pieces can be reused. It'll be really hard to convince them to leggo, as it were. Hmm... leggo... maybe that'd be a good name for it...


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

Well, we want to allow the kids to be able to express themselves. They should be able to build almost anything that they want to. That's why we should start out by giving them just a few small building blocks and some simple rules about how they can be put together, and let them figure out how to make what they want to make.

There's really no way to do this without creating a language. If we just made a finite number of pieces, with no way to combine them together, then we'd just be selling sculptures, not the ability to create your own pieces. If we want them to be able to make things that are as complex as they want, we need to give them a language. 


### Why you?
_What excites you about this idea? How did you come up with it?_

We could make, like, a **lot** of money from this. Parents are suckers for something that'll keep their kids out of their hair for a couple of hours. 


### Domain
_Describe the project's domain in five words._

Building blocks to make stuff.


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user interacts with the language by physically picking up blocks and putting them together. 
Programming in this language looks like hooking blocks together in a particular arrangement. 

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

If the program compiles correctly, parents of the child emit a collective "oooooh". If the program compiles incorrectly, parents of the child emit a disappointed sigh, followed by "your brother was a lot better at this"...

The kinds of errors that can occur are mostly syntax errors, when someone tries to connect the protruding end of a block to the protruding end of another block, or the recessed side to the recessed side of another block.  

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be intuitively easy to put these blocks together to make bigger blocks. Since (at least in the beginning) all the blocks will be brick shaped, it should be tough to make round things like wheels or structures with elements that can move. Maybe we can add that to an expansion pack if this really takes off in the market. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Our closest competitior is probably [Play-Doh](https://en.wikipedia.org/wiki/Play-Doh). It is an admirable language of its own. It is more free-form than our blocks could ever hope to be, which leaves kids with an infinite possibilities of things they can make. However, we have tested the structural integrity of Play-Doh programs, and find them to be lacking compared to our block-based language. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Almost all of the time will be spent engaging in the language aspects of this. We need to figure out how to design the bricks so they can fit together, which basic bricks to provide, how many and which colors to use, what material to make them from, and lots more. So many design decisions to make!

The actual implementation of it should be pretty easy. We just need a couple of designers to mock up some prototypes, a couple million in funding to set up some sweatshops in China, and we'll be off to the races!

### Scope
_How big an idea is this? How ambitious is this project?_

This is a pretty big idea. This will revolutionize the toy industry and change the lives of kids all over the world! We could see a boom in the quantity of artists, sculptors, architects, and engineers as a result of creating this toy.

Since the language's building blocks are a physical product, building this into a business at scale will be quite a challenge. In the design stage, we'll need to carefully think about how to design the blocks as well, because any future blocks we make will need to be backwards compatible with the first generation. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

Note: _I'm writing this from the perspective of myself again, because this question is specific to CS111 and it wouldn't make sense for the Lego designers to be thinking about it._

On the plus side, this idea is all about language design, which is what this class is focused on. 
On the other hand, it's already been done, and not just by the Lego company: Hayden Blauzvern's final project in CS111 last year looks very similar to this. 

