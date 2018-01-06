## Free Proprietary Software Community

# Table of Contents
###### Part I - Technical
* [CCT Information](#cct-information)
   - [Compiler Compiler System (CCS)](#compiler-compiler-system)
   - [Figure of a Traditional Compiler Compiler](#figure-of-a-traditional-compiler-compiler)
   - [Figure of our Compiler Compiler System](#figure-of-our-compiler-compiler-system)
   - [Compiler Compiler System Elements and Rules](#compiler-compiler-system-elements-and-rules)
   - [CCS Syntax-Controlled Runtime API and CCS Syntax-Controlled Binary API](#significance-of-ccs-syntax-controlled-runtime-api-and-ccs-syntax-controlled-binary-api)
   - [Compiler Compiler Technology Terms](#compiler-compiler-technology-terms)
   - [Installation](#installation)
   - [Download](#download)
   - [License](#license)
   - [Patent](#patent)
###### Part II - Non-Technical
 * [Free Proprietary Software Bootstrapping Based on CCT](#free-proprietary-software-bootstrapping-based-on-cct)  
    - [Purpose](#purpose)
    - [Integration](#integration)
###### Part III - Non-Technical
 * [Comparison Analysis](#comparison-analysis)
   - [Artificial Intelligence](#artificial-intelligence)
   - [Internet of Things](#internet-of-things)
   - [Content Management/ Digitization](#content-management)
   - [Platform Platform](#platform-platform)
   - [Blockchain](#blockchain)
   - [Interoperability](#interoperability)
   - [Standardization](#standardization)
   - [Scalability](#scalability)
   - [Security based on Obfuscation](#security-based-on-obfuscation)
   - [Business Model](#business-model)

# CCT Information  

## Compiler Compiler System
[(Back to top)](#table-of-contents)  

*a compiler creating compilers.*  
The CCS is a tool, enabling programs to compile any source code. 
  
The CCS has a specific Source Grammar Definition Language (SGDL), which is  
used as an input to generate a target parser with additional code,  
compiled and linked into an executable program.     
  
After the Compiler Compiler System runs, it creates a program   
that is ready to compile source code and also it is  
ready to generate Compiler Compiler System (CCS) Syntax-Controlled Binary, as well as it is  
ready to decompile the binary to its original definition.     
  
The Compiler Compiler System's important feature of generating  
CCS Syntax-Controlled Binary and then decompling that binary to its   
original form will prove to provide solutions to many technological  
slowdowns: Compilation, Interoperability, Obfuscation, Security,  
Content Management, Scaleability, Standardization.   
These areas, as well as their solutions, will be discussed below.  
  
The Compiler Compiler System is a **tool**.  
  
Being a tool, it is about bettering the lives for software developers.  
  
## Figure of a Traditional Compiler Compiler
[(Back to top)](#table-of-contents)  
![alt text](http://compilercompilertechnology.com/wp-content/uploads/2017/12/Capture.png)



## Figure of our Compiler Compiler System
[(Back to top)](#table-of-contents)  
![alt text](http://compilercompilertechnology.com/wp-content/uploads/2017/12/Capture2.png)

The diagram shows the present invention, The Compiler Compiler System, and its phases for building itself.
The Compiler Compiler executable program, **205**, takes Compiler Compiler Source Grammar Definition Language **201**, 
which defines itself (regarded as meta grammar). **Phase 2.1a**, takes **201** and generates **202**, 
the Compiler Compiler System Syntax-Controlled Runtime. The Compiler Compiler executable program, **205**, 
has an option to de-compile the meta grammar source text from the Compiler Compiler Runtime, shown as **Phase 2.1b**.      
This newly de-compiled meta grammar as a text, is identical to the meta grammar from  
**201** except for some differences related to supported indentation rules.    
 
The Compiler Compiler executable program for the given meta grammar performs **Phase 2.2a**,  
generating the Compiler Compiler Syntax-Controlled Binary, **203**, for the corresponding  
Compiler Compiler Syntax-Controlled Runtime. Phase 2.2a is implemented as a formal procedure that converts  
CCS Syntax-Controlled Runtime into CCS Syntax-Controlled Binary. The Compiler Compiler executable program    
has an option to de-compile the meta grammar, generated from the CCS Syntax-Controlled Binary, into a   
text file (not shown) containing the meta grammar executing phase, **Phase 2.2c**. This newly  
de-compiled meta grammar, as a text, is identical to meta grammar from 201 except for some  
differences related to supported indentation rules.  
  
Having the Compiler Compiler Syntax-Controlled Binary executing phase 2.2b, the Compiler Compiler  
executable program has an option to re-create a Compiler Compiler Syntax-Controlled Runtime that  
is identical to the original Compiler Compiler Runtime from 202. The Compiler Compiler  
executable program performs **Phase 2.3**, creating Compiler Compiler generated code,  
**204** corresponding to the meta grammar from 201.   
  
 ## Significance of CCS Syntax-Controlled Runtime API and CCS Syntax-Controlled Binary API  
[(Back to top)](#table-of-contents)  
  
*The C++ CCS Syntax-Controlled Runtime API is defined in these files:    
include/SyntaxControlledRuntime.h and src/SyntaxControlledRuntime.cc*    
  
*The C++ CCS Syntax-Controlled Binary API is defined in these files:  
include/SyntaxControlledBinary.h and src/SyntaxControlledBinary.cc*  
  
C++ CCS and C CCS both have two implementations of the Parsing Model: Syntax-Controlled Runtime and Binary.  
The Syntax-Controlled Runtime is used by parser performing parsing operations using the corresponding API.  
If the parser is successful at analyzing the source program, the Syntax-Controlled Runtime can be (formally)    
converted to Syntax-Controlled Binary. Any additional semantics processing can be done on Syntax-Controlled Binary  
using the corresponding API. Having a target language description on SGDL, the corresponding parser and additional  
code are generated, when the executable program for the target compiler is built, that compiler program is capable  
of compiling programs on the specified language into Syntax-Controlled Runtime with a subsequent transformation into  
Syntax-Controlled Binary; also that compiler can de-compile the provided Syntax-Controlled Binary file into the original  
source code in accordance with the target language grammar. Ones again, all described operations are completely automated.  
   
## Compiler Compiler Technology Terms  
[(Back to top)](#table-of-contents)  
Meta Grammar  
Source Grammar Definition Language (SGDL)
Compiler Compiler System Syntax-Controlled Runtime API  
Compiler Compiler System Syntax-Controlled Binary API  
Compiler Compiler System Syntax-Controlled Runtime   
Compiler Compiler System Syntax-Controlled Binary  
Compiler Compiler Executable Program  
  
## Meta Grammar Example:  
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
  
Note, that the 'meta' prefix in file names corresponds to the grammar name  
- the first section identifier in SGDL.    
Note also that  
**0 =" METAACTBEG();"=**  
**0 =" METAACTEND();"=**  
are used as a special macro substitution actions defined in form of integer  
number followed by sequence of string  literals enclosed in '=' and '='.       
  
## Compiler Compiler System elements and rules      
[(Back to top)](#table-of-contents)  
The Compiler Compiler Source Grammar Definition Language elements such as '(' and ')'  
are grammar terminals defined as a string literal with enclosed single quotes.  
  
The Compiler Compiler Source Grammar Definition Language consists of a grammar "name"  
section followed by a sequence of rules where the first rule is also a grammar axiom.  
As used  herein, the grammar name section consists of a single identifier that defines a name of grammar.  
  
**The Compiler Compiler Source Grammar Definition Language element:**    
{ rule }  
*is a BNF extension called iteration, meaning that enclosed by { and } 
non-terminal may occur zero or any  other number of times.*  
Note, that, e.g., rule  
         (iterationExample ::= { element } )  
         is equivalent to rules  
         (iterationExample ::= element iterationExample )  
         (iterationExample ::= )  
  
**The Compiler Compiler Source Grammar Definition Language element:**     
 (rule ::= '(' nterm '::=' right ')'  
 )  
*defines rule as a terminal '('  
followed by non-terminal nterm, followed by terminal '::=',  
followed by non-terminal right, followed by terminal ')'.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**    
 (nterm ::= identifier  
 )  
*defines non-terminal nterm as identifier.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (right ::= { element }  
 )  
*defines non-terminal right as an iteration of element non-terminals.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (element ::= identAlt | alternative | identMiss | iteration | action    
 )    
*defines non-terminal element as an alternative of non-terminals on the right side of  
rule definition separated by '|'. The alternative is BNF extension similar to  
iteration extension; it is used in cases when non-terminal on the left side of  
rule definition can be one of non-terminals from the right side.*  
Note, that, e.g., rule  
      (alternativeExample ::= A | B | C | Z )  
      is equivalent to rules  
      (alternativeExample ::= A )  
      (alternativeExample ::= B )  
      (alternativeExample ::= C )  
      (alternativeExample ::= Z )
  
 **The Compiler Compiler Source Grammar Definition Language element:**  
 (action ::= integerToken '=' { stringToken } '='  
 )  
*defines non-terminal action as an integerToken followed by terminal '=',  
followed by iteration of stringToken followed by terminal '='. Here integerToken   
and stringToken are another Compiler Compiler Source Grammar Definition Language  
reserved key words similar to identifier. integerToken defines token that holds  
integer value. stringToken defines token that holds string literal value as an  
arbitrary sequence of any characters enclosed with double quotes, i.e., ".*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (actions ::= '=' { action } '='  
 )  
*defines non-terminal actions as a iteration of action enclosed with '='.*    
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (identAlt ::= ntermtermact { Altpart }  
 )  
*defines non-terminal identAlt as a ntermtermact followed by iteration of Altpart non-terminals.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (Altpart ::= '|' ntermtermact  
 )  
*defines non-terminal Altpart as a terminal '|' followed by non-terminal ntermtermact.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**    
 (ntermtermact ::= ntermterm [ actions ]  
 )  
*defines non-terminal ntermtermact as a non-terminal ntermterm followed by [ actions ] meaning that  
non-terminal actions may be omitted. Non-terminal enclosed with [ and ] is another compiler compiler  
source grammar definition language BNF extension representing elements that can be omitted.*  
Note, that, e.g., rule  
      (ommitedElementExample ::= A [ W ])  
      is equivalent to rules:  
      (ommitedElementExample ::= A Welement )    
      (Welement::= W )  
      (Welement::= )  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (ntermterm ::= nterm | termToken  
 )  
*defines non-terminal ntermterm as an alternative of nterm of termToken. nterm is defined above.  
termToken is another compiler compiler source grammar definition language reserved key word that defines    
terminal token specification as a string literal enclosed with single quotes.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (alternative ::= '(' identAlt ')'  
 )  
*defines non-terminal alternative as an identAlt enclosed with terminals '(' and ')'.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (identMiss ::= '[' identAlt ']'  
 )  
*defines non-terminal identMiss as an identAlt enclosed with terminals '[' and ']'.*   
  
**The Compiler Compiler Source Grammar Definition Language element:**        
 (iteration ::= '{' iterItemact iterItems '}'  
 )   
*defines non-terminal iteration as an iterItemact followed by non-terminal iterItems enclosed with  
terminals '{' and '}'.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**        
 (iterItems ::= { altIterItem }  
 )  
*defines non-terminal iterItems as an iteration of altIterItem non-terminals.*    
  
**The Compiler Compiler Source Grammar Definition Language element:**       
 (altIterItem ::= '|' iterItemact  
 )  
*defines non-terminal altIterItem as terminal '|' followed by non-terminal iterItemact.*  
  
**The Compiler Compiler Source Grammar Definition Language element:**       
 (iterItemact ::= iterItem [ actions ]  
 )  
*defines non-terminal iterItemact as non-terminal iterItem followed by [ actions ].*   
  
**The Compiler Compiler Source Grammar Definition Language element:**      
 (iterItem ::= nterm | maybeNterm  
 )  
*defines non-terminal iterItem as an alternative of non-terminals nterm and maybeNterm.*    
  
**The Compiler Compiler Source Grammar Definition Language element:**     
 (maybeNterm ::= '<' nterm '>'  
 )  
*defines non-terminal maybeNterm as non-terminal nterm enclosed between terminals '<' and '>'.*  
  
The compiler compiler source grammar definition language iteration is actually defined as  
a sequence of terminals or nonterminals may be followed by actions, and also non-terminals  
may be enclosed between terminals '<' and '>' meaning that such non-terminal is allowed to  
be in iteration only zero or one time.     
Note, that, e.g., the rule  
      (anotherIterationExampe :: = { A | B | <X> | <Z> } )  
      is equivalent to the rules  
      (anotherIterationExampe :: = elem anotherIterationExampe )  
      (anotherIterationExampe :: = )  
      (elem ::= A | B | X | Z )  
  
## Download  
//zip (after edit)

## Installation  
//clean up installment-> Download Instructions  
Download Video  
  
## License    
[License](http://compilercompilertechnology.com/wp-content/uploads/2018/01/FreeProprietarySoftwareLicense.pdf)
  
   
## Patent  
[Patent](http://compilercompilertechnology.com/wp-content/uploads/2017/03/US-08464232.pdf)  
    
[(Back to top)](#table-of-contents)  
---  
  
---  
# Free Proprietary Software Bootstrapping Based on CCT
  
## Purpose
     
## Integration  
1) light router
2) compiler compilers system repository
3) integration based on 1 and 2
  
[(Back to top)](#table-of-contents)  
---  
  
---  
# Comparison Analysis
  
### Technology is growing vastly with promising advancements however we see through AI, IoT, and various other technologies, we face bottlenecks and setbacks that help us further move forward into a completely scalable, interoperable technological society. ###
  
### Let's take AI specifically as an example; "Experts estimate that AI market will increase from the $200 billion it is valued today to $3.1   trillion by 2025, but serious roadblocks remain." Today, AI functionality is expensive, time-consuming, and hard to use and is among one of many technologies with similar experiences. ###
  
### In the following section, we will underly how Compiler Compiler Technology will eradicate these problems completely, solving problems with standardizaton and interoperability, creating a completely scalable technological world in all areas. Solutions to these problems enable the creation of trillions of $US in value but also help us further the advancements of mankind. ###
  
## Artificial Intelligence
  
## Internet of Things
 
## Content Management/ Digitization

## Platform Platform
  
## Blockchain
  
## Interoperability
  
## Standardization
  
## Scalability
  
## Security Based On Obfuscation
  
## Business Model
   
[(Back to top)](#table-of-contents)  
---  
  
---   



