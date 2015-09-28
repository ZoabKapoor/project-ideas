# Free project 2

_Note: this DSL is actually two languages in one: one to program an automatic coffee machine and one to program an alcoholic drink mixer. Since they're so similar, I'm writing about a language to specify specialty drinks in general, and will pick one of the two (since a combined coffee machine/drink maker isn't likely to be created anytime soon) to implement if I decide on this project idea._

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

_Credit to Axel at [Drip City Coffee](http://dripcitycoffee.com/) for helping me with this idea. When I spoke to him about it, I was thinking of only making a language to specify coffee drinks, but he argued that a language for alcoholic drinks would be even better. The reason for this, he purported, is because coffee drinks are harder have a machine make well than alcoholic ones (which I agree with, I've never drank a coffee from an automatic machine which was better than one made by a real barista), so a language for specifying arbitrary alcohol drinks would be more likely to disrupt the bartending industry than an equivalent language for coffee._

Coffee drinks are difficult to make. In the world of the ever-present hipster, it's getting harder and harder to get it just right. In a world where customers actually order a "split-shot, heavy on decaf, 20 oz, soy, extra dry latte, with half pump vanilla & half-pump hazlenut", keeping track of all the modifications to make for a coffee drink is a difficult experience for a physical barista In addition, most automatic coffee machines have a finite amount of settings that a customer can customize. 

Alcoholic beverages present a similar challenge. The barista I was discussing this project idea with told me about his favourite drink: "Old fashioned, with 2 shots of rye whisky, cane syrup instead of brown sugar, extra bitters, and orange zest instead of an orange slice". 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_


### Why you?
_What excites you about this idea? How did you come up with it?_


### Domain
_Describe the project's domain in five words._

Making specialty coffee/alcoholic drinks.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

Each line of code will be run sequentially. For instance, if a user says
```
1. A shot of whiskey
2. A shot of plain vodka
```
the resultant drink will have a darker hue on the top than if the two steps were reversed. 


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_


### Scope
_How big an idea is this? How ambitious is this project?_


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

