# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Picture this: A student, sitting in her room at 12:14 PM. HMC's registration portal is open on her laptop. Her registration starts in a minute. She knows that two of the classes she wants to take have only a few seats left in them. The clock strikes 12:15. She makes a choice, and regretfully clicks the search button on the portal. After a few agonizing seconds, she gets redirected back to the portal's search page. "You shouldn't have clicked refresh", the angry red text says. Confused, she navigates back to the course she wanted. By that time, both courses are filled up. She shakes her fist at the heavens and curses the portal.

But what if there was a better way? What if she could instead compile a list of her favourite classes (in order of importance) a few days earlier and send it to the registrar. The registrar would compile this list from all students, and then sort students into their preferred classes in order of registration time, breaking ties randomly. And people wouldn't get locked out of classes they want to take because portal decided to crash on them randomly. 

### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

If we had a better course registration system, then this DSL might not be necessary at all. However, I believe we're under contract with the company that makes our portal, so we won't be able to switch away from it for the next few years at least.

First, I'll talk about some of the alternative solutions to the problem, and why they're not as good (in my opinion) as a DSL. 

One way to solve this problem would be to do what the CS department did last semester by sending out a pre-registration survey to all students. However, one of the UX problems with the survey was that it was very verbose. I think writing a program in this language would be a more succint way to convey your registration intentions. In addition, I don't know what tools Google provides to parse the results of Google Forms, but if the results had to be manually compiled that would cost a lot of person-hours. 

Another alternative way to solve the problem would be to just have the registrar manually compile lists of people's desired classes. However, in a school of 800 people this would be an immensely time consuming process, and prone to user error. Automating the process would be much simpler, which would require people's class lists to be easily parsable. Having them write these lists using a particular structure (specifically, the structure of this DSL) would make the parsing job much simpler. 

Since everyone at Mudd has taken CS5 or CS42, they all have experience dealing with a small DSL (Picobot). I think it wouldn't be hard for people to learn how to write a program in this DSL. It addresses the need by allowing people to register for classes while bypassing the downsides of using the portal directly, which I think is exactly what people want.  

### Why you?
_What excites you about this idea? How did you come up with it?_

The portal is possibly the most hated piece of software among Mudders. Coming up with a better alternative would make a lot of people (including myself) a lot happier. One of my priorities in this final project is building something that would actually make people's lives better, and I think that building this system would make Mudders a lot less stressed about registration.

### Domain
_Describe the project's domain in five words._

Like the portal, but better.

### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

This is what I imagine a sample program might look like:

```
Name: Joe Platt

I want to register for [range] credits;
I want to register for these classes:
    1. DSLs
    2. LSD (Software Development)
    3. LDS (Intro to Mormonism)
    ... etc
```

Where [range] is a numeric range of credits whose lower bound is 12 and upper bound is 18. 

### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

Note that running this program wouldn't directly enroll a student in classes. Instead, it would put their preferences into some central database of preferences. In particular, I'm imagining that every class would have a "waiting list" into which a student would go if they listed the class in their preferences. 

Then, there would be another program that actually sorts students into classes by taking people off the waiting list in order of priority (and breaking ties randomly). This program would then either directly interface with the portal and reserve that many seats for pre-registered students or print out a list of classes and how many seats to reserve for the registrar to take care of manually. 

The only kind of error that can occur in this case would be parse errors, where a program doesn't adhere to the structure expected by the parser. These could be either syntax errors, where the program isn't formatted correctly, or runtime errors where, for instance, a class can't be found. These could be communicated to the user by throwing the appropriate type of exception - for instance, a ClassNotFound exception if the class the user wants to register for doesn't exist, or NameNotFound exception if the user forgot to enter their name or their name doesn't exist in the list of HMC students.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

The expressiveness of this lanugage is very limited. It should be easy to specify the classes and number of credits you want to register for, and to specify your identifying information. It should be impossible to do anything else.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

There are no other DSLs in this domain that I know of. I imagine there aren't any because the domain is really small - for all we know, it could be just Mudd that has to deal with a terrible registration portal. 


## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Because programs in this language have such simple syntax, I imagine most of someone's time spent on thier project would be working on the "systems" aspect of the project. However, because the lanugage (at least right now) has natural language (English) embedded in it, building the parser (which I consider part of the language aspects of the project) could be a difficult thing to do.


### Scope
_How big an idea is this? How ambitious is this project?_

While the language itself will be pretty small, the project would be fairly difficult to actually implement. This is largely because creating and implementing the models used on the backend (the agggregator for student choices, and the pre-registrator code) would be fairly difficult. However, I think that an impementer could successfully implement this project end-to-end in half a semester. 

### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

I think this would be a good idea for a project because it directly solves a problem experienced by the immediate population. 
The benefits of this are twofold: 
1. The implementer can easily gather user requirements/feature requests as they build the project.
2. We know for sure that there will be a user base for this DSL. 

There are also two main reasons why this might not be a good project idea:
1. As mentioned earlier, the implementer would probably spend a lot more time engaging in the systems aspect of the language than the design aspect. Since this class seems to be focused on language design in a big way, this project may not be best at fulfilling the learning goals of the class.
2. Even if this language did exist, the bureaucracy required to get anything done with Mudd's administration may be a prohobitively large barrier to actually adopting this system.

I think the main tradeoff in terms of deciding whether to implement this project is the tradeoff between spending a lot of time on language design (which is more in line with this class's goals) and building something that would be really useful to Mudders. 