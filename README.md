# cctToken, using Compiler Compiler Technology

## Compiler Compiler System (CCS): a compiler creating compilers.

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

The Compiler Compiler System is a **tool**.

Being a tool, it is about bettering the lives for software developers.


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
