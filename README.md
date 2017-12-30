# cctToken, using Compiler Compiler Technology
License (Links)
US Patent (Links)

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

## Figure of a Traditional Compiler Compiler
![alt text](http://compilercompilertechnology.com/wp-content/uploads/2017/12/Capture.png)



## Figure of our Compiler Compiler System
![alt text](http://compilercompilertechnology.com/wp-content/uploads/2017/12/Capture2.png)

A compiler compiler executable program, 205, takes compiler compiler
source grammar definition language source text defining itself
(meta grammar), 201, and performs a phase 2.1a,
generating compiler compiler runtime, 202, for the meta grammar from 201.
Compiler compiler executable program, 205, has an option to 
de-compile the meta grammar generated compiler compiler runtime, 202, 
into a text file (not shown) containing the meta grammar executing phase, 2.1b. 
This newly de-compiled meta grammar as a text is identical to the meta grammar 201 
except for some differences related to supported indentation rules.

Compiler compiler executable program 205 for meta grammar 201 performs phase 2.2a generating compiler
compiler binary 203 for compiler compiler runtime 202. The phase 2.2a is implemented as a formal procedure that
converts compiler compiler runtime 202 into compiler compiler binary 203. Compiler compiler executable program
205 has an option to de-compile meta grammar from generated compiler compiler binary 203 into a text file (not
shown) containing meta grammar executing phase 2.2c. This newly de-compiled meta grammar as a text is identical
to meta grammar 201 except for some differences related to supported indentation rules. Compiler compiler
executable program 205 has an option to re-create a compiler compiler runtime that is identical to original compiler
compiler runtime 202 having compiler compiler binary 203 executing phase 2.2b.

Compiler compiler executable program 205 performs phase 2.3 creating a compiler compiler generated code 204
corresponding to meta grammar 201. The compiler compiler source grammar definition language consists of a
grammar name section followed by a sequence of rules where the first rule is also a grammar axiom. As used
herein, the grammar name section consists of a single identifier that defines a name of grammar. 


## As an example,
When C++ compiler compiler executable program 205 takes the following meta grammar source file:  
(meta  
   (grammar ::=  
      0 =" METAACTBEG();"=  
      '(' grammarNameDef  
          { rule }  
       ')'  
        0 =" METAACTEND();"=  
 )  
 (grammarNameDef ::= identifier  
 )  
 (rule ::= '(' nterm '::=' right ')'  
 )  
 (nterm ::= identifier  
 )  
 (right ::= { element }  
 )
 (element ::= identAlt | alternative | identMiss | iteration | action  
 )  
 (action ::= integerToken '=' { stringToken } '='  
 )  
 (actions ::= '=' { action } '='  
 )  
 (identAlt ::= ntermtermact { Altpart }  
 )  
 (Altpart ::= '|' ntermtermact  
 )  
 (ntermtermact ::= ntermterm [ actions ]  
 )  
 (ntermterm ::= nterm | termToken  
 )  
 (alternative ::= '(' identAlt ')'  
 )  
 (identMiss ::= '[' identAlt ']'  
 )  
 (iteration ::= '{' iterItemact iterItems '}'  
 )  
 (iterItems ::= { altIterItem }  
 )  
 (altIterItem ::= '|' iterItemact  
 )  
 (iterItemact ::= iterItem [ actions ]  
 )  
 (iterItem ::= nterm | maybeNterm  
 )  
 (maybeNterm ::= '<' nterm '>'  
 )  
)  


As a result of phase 2.3 the following C++ source files are generated:
- metaGenerator.h
- metaKeyWordDefinition.h
- metaParser.h
- metaGenerator.cc
- metaKeyWordDefinition.cc
- metaParser.cc
- metaMakeGenerators.cc

Note, that the 'meta' prefix in file names corresponds to the grammar name - the first section identifier in source
grammar definition language. 
Note also that
**0 =" METAACTBEG();"=**
**0 =" METAACTEND();"=**
are used as a special macro substitution actions defined in form of integer number followed by sequence of string
literals enclosed in '=' and '='. 

## Compiler Compiler System elements and rules:  
The compiler compiler source grammar definition language elements such as '(' and ')' are grammar terminals  
defined as a string literal with enclosed single quotes.   
  
**The compiler compiler source grammar definition language element:**  
{ rule }  
*is a BNF extension called iteration, meaning that enclosed by { and } non-terminal may occur zero or any
other number of times.*  
***Note, that, e.g., rule  
         (iterationExample ::= { element } )  
         is equivalent to rules  
         (iterationExample ::= element iterationExample )  
         (iterationExample ::= )  

**The compiler compiler source grammar definition language rule:** 
 (rule ::= '(' nterm '::=' right ')'  
 )  
*defines rule as a terminal '(' followed by non-terminal nterm followed by terminal '::=' followed by non-terminal  
right followed by terminal ')'. *

**The compiler compiler source grammar definition language rule:**
 (nterm ::= identifier  
 )  
*defines non-terminal nterm as identifier. * 

**The compiler compiler source grammar definition language rule:**  
 (right ::= { element }  
 )  
*defines non-terminal right as an iteration of element non-terminals.*  

**The compiler compiler source grammar definition language rule:**  
 (element ::= identAlt | alternative | identMiss | iteration | action  
 )  
*defines non-terminal element as an alternative of non-terminals on the right side of rule definition separated by '|'.  
The alternative is BNF extension similar to iteration extension; it is used in cases when non-terminal on the left side
of rule definition can be one of non-terminals from the right side.*
***Note, that, e.g., rule  
      (alternativeExample ::= A | B | C | Z )  
      is equivalent to rules  
      (alternativeExample ::= A )  
      (alternativeExample ::= B )  
      (alternativeExample ::= C )  
      (alternativeExample ::= Z )***

**The compiler compiler source grammar definition language rule:**  
 (action ::= integerToken '=' { stringToken } '='  
 )  
*defines non-terminal action as an integerToken followed by terminal '=' followed by iteration of stringToken  
followed by terminal '='. Here integerToken and stringToken are another compiler compiler source grammar  
definition language reserved key words similar to identifier. integerToken defines token that holds integer value.  
stringToken defines token that holds string literal value as an arbitrary sequence of any characters enclosed with  
double quotes, i.e., ".  *

**The compiler compiler source grammar definition language rule:**  
 (actions ::= '=' { action } '='  
 )  
*defines non-terminal actions as a iteration of action enclosed with '='.*  

**The compiler compiler source grammar definition language rule:**  
 (identAlt ::= ntermtermact { Altpart }  
 )  
*defines non-terminal identAlt as a ntermtermact followed by iteration of Altpart non-terminals.*  

**The compiler compiler source grammar definition language rule:**  
 (Altpart ::= '|' ntermtermact  
 )  
*defines non-terminal Altpart as a terminal '|' followed by non-terminal ntermtermact.*  

**The compiler compiler source grammar definition language rule:**  
 (ntermtermact ::= ntermterm [ actions ]  
 )  
*defines non-terminal ntermtermact as a non-terminal ntermterm followed by [ actions ] meaning that non-terminal  
actions may be omitted. Non-terminal enclosed with [ and ] is another compiler compiler source grammar definition  
language BNF extension representing elements that can be omitted. *
***Note, that, e.g., rule  
      (ommitedElementExample ::= A [ W ])  
      is equivalent to rules:  
      (ommitedElementExample ::= A Welement )  
      (Welement::= W )  
      (Welement::= )***  

**The compiler compiler source grammar definition language rule:**  
 (ntermterm ::= nterm | termToken  
 )  
*defines non-terminal ntermterm as an alternative of nterm of termToken. nterm is defined above.  
termToken is another compiler compiler source grammar definition language reserved key word that defines  
terminal token specification as a string literal enclosed with single quotes.*  

**The compiler compiler source grammar definition language rule:**  
 (alternative ::= '(' identAlt ')'  
 )  
*defines non-terminal alternative as an identAlt enclosed with terminals '(' and ')'.*  

**The compiler compiler source grammar definition language rule:**  
 (identMiss ::= '[' identAlt ']'  
 )  
*defines non-terminal identMiss as an identAlt enclosed with terminals '[' and ']'.*  

**The compiler compiler source grammar definition language rule:**  
 (iteration ::= '{' iterItemact iterItems '}'  
 )   
*defines non-terminal iteration as an iterItemact followed by non-terminal iterItems enclosed with 
terminals '{' and '}'.*  

**The compiler compiler source grammar definition language rule:**  
 (iterItems ::= { altIterItem }  
 )  
*defines non-terminal iterItems as an iteration of altIterItem non-terminals.*  

**The compiler compiler source grammar definition language rule:**  
 (altIterItem ::= '|' iterItemact  
 )  
*defines non-terminal altIterItem as terminal '|' followed by non-terminal iterItemact. * 

**The compiler compiler source grammar definition language rule:**  
 (iterItemact ::= iterItem [ actions ]  
 )  
*defines non-terminal iterItemact as non-terminal iterItem followed by [ actions ].*  

**The compiler compiler source grammar definition language rule:**  
 (iterItem ::= nterm | maybeNterm  
 )  
*defines non-terminal iterItem as an alternative of non-terminals nterm and maybeNterm.*  

**The compiler compiler source grammar definition language rule:**  
 (maybeNterm ::= '<' nterm '>'  
 )  
*defines non-terminal maybeNterm as non-terminal nterm enclosed between terminals '<' and '>'. *  

The compiler compiler source grammar definition language iteration is actually defined as a sequence of terminals or nonterminals
may be followed by actions, and also non-terminals may be enclosed between terminals '<' and '>'
meaning that such non-terminal is allowed to be in iteration only zero or one time.   
Note, that, e.g., the rule  
      (anotherIterationExampe :: = { A | B | <X> | <Z> } )  
      is equivalent to the rules  
      (anotherIterationExampe :: = elem anotherIterationExampe )  
      (anotherIterationExampe :: = )  
      (elem ::= A | B | X | Z )  


























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
