# cctToken, using Compiler Compiler Technology

## Compiler Compiler System
compiler compiler system (CCS): a compiler creating compilers.

The CCS is a tool, enabling programs to compile any source code. 

The CCS has a specific source grammar definition language, which is
used as an input to generate a target parser with additional code,
compiled and linked into an executable program. 

After the Compiler Compiler System runs, it creates a program 
that is ready to compile source code and also it is
ready to generate syntax controlled binary, as well as it is
ready to decompile binary to its original definition. 

The Compiler Compiler System's important feature of generating
syntax controlled binary and then decompling that binary to its 
original form will prove to provide solutions to many technological
slowdowns; Compilation, Interoperability, Obfuscation, Security,
Content Management, Scaleability, Standardization.
These areas, as well as their solutions, will be discussed further down.

re-frame is a pattern for writing [SPAs] in ClojureScript, using [Reagent].

McCoy might report "It's MVC, Jim, but not as we know it".  And you would respond 
"McCoy, you trouble maker, why even mention an OO pattern? 
re-frame is a **functional framework**."

Being a functional framework, it is about data, and the functions 
which transform that data.

## Why Should You Care?

Perhaps:

1.  You want to develop an [SPA] in ClojureScript, and you are looking for a framework.
2.  You believe Facebook did something magnificent when it created React, and
    you are curious about the further implications. Is the combination of
    `reactive programming`, `functional programming` and `immutable data` going to
    **completely change everything**?  And, if so, what would that look like in a language
    that embraces those paradigms?
3.  You're taking a [Functional Design and Programming course](http://www.eli.sdsu.edu/courses/fall15/cs696/index.html) at San Diego State University
    and you have a re-frame/reagent assignment due.  You've left the reading a bit late, right?
4.  You know Redux, Elm, Cycle.js or Pux and you're
    interested in a ClojureScript implementation.
    In this space, re-frame is very old, hopefully in a Gandalf kind of way.
    First designed in Dec 2014, it even slightly pre-dates the official Elm Architecture,
    although thankfully we were influenced by early-Elm concepts like `foldp` and `lift`, as well as 
    Clojure projects like [Pedestal App], [Om] and [Hoplon]. Since then,
    re-frame has pioneered ideas like event handler middleware,
    coeffect accretion, and de-duplicated signal graphs.
5.  Which brings us to the most important point: **re-frame is impressively buzzword compliant**. It has reactivity,
    unidirectional data flow, pristinely pure functions,
    interceptors, coeffects, conveyor belts, statechart-friendliness (FSM)
    and claims an immaculate hammock conception. It also has a charming
    xkcd reference (soon) and a hilarious, insiders-joke T-shirt,
    ideal for conferences (in design).  What could possibly go wrong?

[OM]:https://github.com/swannodette/om
[Hoplon]:http://hoplon.io/
[Pedestal App]:https://github.com/pedestal/pedestal-app


## It Leverages Data

You might already know that ClojureScript is a modern Lisp, and that
Lisps are **homoiconic**.  If not, you do now.

This homoiconic bit is significant. It means you program in a Lisp by creating and
assembling Lisp data structures. Dwell on that for a moment. You are **programming in data**. 
The functions which later transform data, themselves start as data.

Clojure programmers place particular emphasis on the primacy of data, and 
they like to meditate on aphorisms like **data is the ultimate in late binding**. 
(Less productively, they also like re-watching Rich Hickey videos, and wishing
their hair was darker and more curly)

I cannot stress enough what a big deal this is. It may seem 
like a syntax curiosity at first but, when the penny drops for 
you on this, it tends to be a profound moment. And once you 
understand the importance of this concept at the language level, 
you naturally want to leverage similar power at the library and system levels.

So, it will come as no surprise, then, to know that re-frame has a 
data oriented design. Events are data. Effects are data. DOM is data.
The functions which transform data are registered and looked up via 
data. Interceptors (data) are preferred over middleware (higher 
order functions). Etc. 

**Data - that's the way we roll.**


## It is a loop

Architecturally, re-frame implements "a perpetual loop".

To build an app, you hang pure functions on certain parts of this loop, 
and re-frame looks after the **conveyance of data** 
around the loop, into and out of the transforming functions you 
provide - hence a tag line of "Derived Values, Flowing".

### It does Physics
