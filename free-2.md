# Free project 2

_Note: this DSL is actually two languages in one: one to program an automatic coffee machine and one to program an alcoholic drink mixer. Since they're so similar, I'm writing about a language to specify specialty drinks in general, and will pick one of the two (since a combined coffee machine/drink maker isn't likely to be created anytime soon) to implement if I decide on this project idea._

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

_Credit to Axel at [Drip City Coffee](http://dripcitycoffee.com/) for helping me with this idea. When I spoke to him about it, I was thinking of only making a language to specify coffee drinks, but he argued that a language for alcoholic drinks would be even better. The reason for this, he purported, is because coffee drinks are harder have a machine make well than alcoholic ones (which I agree with, I've never drank a coffee from an automatic machine which was better than one made by a real barista). Thus, a language for specifying arbitrary alcohol drinks would be more likely to disrupt the bartending industry than an equivalent language for coffee._

Coffee drinks are difficult to make. In the world of the ever-present hipster, it's getting harder and harder to get it just right. In a world where customers actually order a "split-shot, heavy on decaf, 20 oz, soy, extra dry latte, with half pump vanilla & half-pump hazlenut", keeping track of all the modifications to make for a coffee drink is a difficult experience even for a physical barista. On the other hand, automatic coffee machines have a finite amount of settings that a customer can customize. 

Alcoholic beverages present a similar challenge. The barista I was discussing this project idea with told me about his favourite drink: "Old fashioned, with 2 shots of rye whisky, cane syrup instead of brown sugar, extra bitters, and orange zest instead of an orange slice". 

If there was a standard language by which a customer could specify a drink to an arbitrary level of precision, then you could easily program an automatic coffee machine or autobartender to make exactly the drink you want. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

We need a DSL for this because we want to enable users to specify their drinks to arbitrary levels of precision. There are so many factors that go into a caffeinated or alcoholic beverage that we need a language (rather than, for instance, an enumerated type), because there are just so many possibilities. I imagine that there would be a GUI for end users to interact with this system, but compiling to a DSL built specifically for this purpose (sadly, CoffeeScript is already taken) seems advantageous. 

### Why you?
_What excites you about this idea? How did you come up with it?_

I **love** coffee, so I'd be really excited to actually make this kind of thing. Amusingly (and probably not coincidentally), I came up with it while sitting in a coffee shop. As I mentioned earlier, the barista I discussed it with (we got onto this topic when I asked him what the most complicated drink he's ever been asked to make was) suggested making the language apply to alcoholic drinks instead, because they're easier to make (for reasons which I can discuss in person with anyone whose interested; it's not the focus of this assignment).


### Domain
_Describe the project's domain in five words._

Making specialty caffienated/alcoholic drinks.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

A user could write a program directly in this language, or interact with it through a GUI similar to the ones present in some modern automatic coffee machines. For maximum customizability, I would recommend that a user just write a program directly in the language.

A program might look something like this:
```
Begin LATTE:
1. 2 shots espresso
2. Add 10 oz 2% milk
3. Add 2 oz very hot steam
4. Add 4 pumps sugar
End LATTE:
```

Or like this:

```
Begin PUMPKIN_SPICE_LATTE:
1. LATTE
2. Add 2 pumps pumpkin
3. Add 1 shake Cinnamon
~~4. Add judgement~~
End PUMPKIN_SPICE_LATTE
```

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

Syntax errors are, of course, always possible. I'm not sure what kind of semantics errors might occur. Theoretically, one could just allow any code written in the language to execute, no matter how nonsensical it seems. Alternatively, you could build some semantic analysis into the language - for example, throwing an exception if a coffee drink is being made but no step to add coffee is included.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There aren't any other DSLs in this domain that I know of. Automated coffee machines already have a GUI that lets you customize your drink in this way but

1. It almost certainly doesn't compile to a DSL (though maybe it does)
2. The language has limited expressiveness. You can choose a base drink, and then modify the amount of coffee, sugar, and milk to add, but that's about it. The language I'm proposing would allow you to create a drink from the bottom up. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think they'd be spending a lot of time making language design decisions, but also a fair amount of time implementing the language. One of the interesting decisions they'll have to make is figuring out what the deliverable _for this class_ will be - we obviously won't have access to an automated coffee machine or alcohol mixer (do those even exist?) to try it out on, so there would have to be some other deliverable to present when someone runs a program in this language.


### Scope
_How big an idea is this? How ambitious is this project?_

I'd call this a medium sized idea. Implementing it is going to be difficult (because there will be a lot of language design choices to make), but I think it'll be manageable over the course of the semester.

If I choose to attempt to monetize it, **that** would be ambitious. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think it would be a great idea for a project for me, because I'm very excited about coffee and I think it could ultimately be a really useful language. The downsides of this project are that it's a bit on the large side and it would be hard to work out what the deliverable of the project would be. 

