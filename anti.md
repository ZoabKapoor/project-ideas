# Anti project

_Note: Though I think that this wouldn't work as a final project for DSLs, I still think it'd be pretty awesome to implement in general._

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

I feel like the code debugging experience is rarely optimal. Though modern technology has progressed so far, I've never been able to find a debugger that does exactly what I want it to do. In particular, I want a debugger that runs a program start to finish and then generates a tree of the commands run. Then, I'd want to be able to navigate that tree, moving back and forth (as well as stepping in and out of functions) at will, all while being able to see the values of various variables of interest. Where this diverges from what debuggers can do normally is as follows: debuggers that I've worked with (I'm thinking of the Eclipse and Gnu debuggers in particular) generally have an instruction pointer that points to the particular line of code about to be executed. While this pointer can move forward easily, going back in the code is a much more difficult process.

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

It's not. A DSL that solves this problem's only function would be to let a user navigate the tree. It would only have 4 commands: step in, step out, step over [optional: n times], and step back [optional: n times]. Ideally, the user would interact with the debugger using a GUI (specifically, with a point-and-click mechanism), but it would just be stepping around under the hood. In any case, a DSL with only 4 words seems too limited to be an interesting final project. 

### Why you?
_What excites you about this idea? How did you come up with it?_

I think that this idea would make my debugging process, and hopefully that of many other software developers, a lot easier. I'd still be interested in making this someday, just not for this class.

### Domain
_Describe the project's domain in five words._

Debuggers can step backwards now!

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

The user would first boot up the application and give it a program to debug. She would then interact with the application by clicking on a particular line of code to see what the values of initialized variables are at that line. The user could then double click to step into the line (if it's a function call), right click (or some keybord shortcut) to step out, or click on another line in the same function to investigate it. 

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the application is booted up, the code to be debugged is run, with all function calls and variables tracked through the running process. Then, a navigable tree would be built based on the execution history and displayed to the user for her viewing pleasure. 

I really hope no errors would occur here, since debugging a debugger sounds like no fun. I guess there could be syntax errors if the "program" passed into the debugger isn't actually a program.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

I don't really know what to say here. It should be easy to debug code and impossible to do anything else. 

### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are certainly other debuggers, and there may even be others with rewind functions. However, all of the debuggers I've worked with lack this function. I found a [debugger](http://debug.elm-lang.org/) online that does everything I want this debugger to do better than I ever could, however it appears to only be for the [Elm language](http://elm-lang.org/). 

An aside: Interestingly enough, this debugger was inspired by Bret Victor's [Inventing on Principle](https://www.youtube.com/watch?v=PUv66718DII), which we watched on our first day of class. Cool! 

Aside from Elm, however, it seems like the space for time-travelling debuggers in most other programming languages is mostly unexplored.

## The Project
This section examines whether the idea makes for a good CS 111 project.

### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Virtually no time would be spent on the language design aspect, and they'd probably have to spend a lot of time working on the "systems" aspects of the project (Writing a debugger, even as a wrapper on top of another debugger, is **hard**!).

### Scope
_How big an idea is this? How ambitious is this project?_

While the language itself is small, the ambitiousness of this as a coding project is **massive**. Just doing this for one language would be tough at best, and there are **so many** languages that could use a debugger that can rewind. 


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This wouldn't be a good idea for the DSLs final project because it would be:

1. Hard. Like, really hard. I'm skeptical I'd be able to finish by the end of the semester if I did try to build it.
2. Not very involved as far as language design goes. 

That said, it seems like it would be a really cool thing to have! I may try to implement it on my own time outside of this class (and by outside of class, I mean outside of Mudd, because let's be real, I don't have the time to take on a coding project of that magnitude while giving my classwork the attention it deserves). 