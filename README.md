#Why?
- This is my treasure Im willing to share. I have all the links 
## Python:
- Is general purpose programing language used for:
  - Web development server side
  - software development and workflows, data management
  - mathematics
  - system scripting
  - [src](https://www.w3schools.com/python/python_intro.asp).
- Python:
  - has a simple syntax that allows you to program in fewer lines of code.
  - is easy to learn
  - it can be both either functional and object-oriented
  - it is ideal for data mining and data facilitation
  - good community support
  - 
- Installation and setup:
  - Download [anaconda](https://www.anaconda.com/products/individual)
-Data Type:
  - Text type: str
  - Numeric Types: int, float, complex
  - Sequence Type: list, tuple, range
  - Mapping Type: dict
  - Set type: bool
  - Binary Types: bytes, bytearray, memoryview
  - [reference](https://docs.python.org/3/library/stdtypes.html?highlight=data%20types)
    - To get the datatype, use the type() function.
- Structure:
  - Python lets us split the program into modules that can be reused.
  - It is interpreted
  - It is extensible
- Start:
  - start by checking if you have python installed properly
  - `python --version`
  - `python` will launch python
  - to quit , type `quit()`
- Implementations:
  - CPython - written in C
  - JPython - Written in Java
  - Python for .NET - written in C but is a managed .NET application
  - IronPython - an alternative to Python.NET, providing availability to .NET libraries, also generate IL and compiles pyton code directly to .NET assemblies.
  - PyPy - written completely in Python.
- Notation:
  - modified BNF grammar notation
    - [BNF](http://www.cs.umsl.edu/~janikow/cs4280/bnf.pdf) or Backus-Naur Form is used to define syntax using:
      - a set of terminal symbols
      - a set of non-terminal symbols
      - a set of production rules of the form `Left-Hand-Side ::= Right-Hand-Side`
        - Left-hand side contains non terminal 
        - Right-hand side contains either terminal or non-terminal or both.
          - left-hand side can be replaced by the right-hand expression
          - syntactical correct sentences follow the above-mentioned order.
          - if a parse tree cannot be built to show the sentence derives from the production rules, the sentence is deemed syntactically incorrect.
    - ####Grammar:
      - A sentence can be well-formed but still meaningless.
      - Semantics will define the meaning.
    - [sources](https://docs.python.org/3/reference/introduction.html#implementations)
      - ####Example
        - A grammar that recognizes exactly two strings `things are getting better` and `things are getting worse`
    
        ```
      
      
        things ::= "things are" condition
           condition ::= "getting better" | "getting worse"  
                           things
                           /     \
                          /       \
            "things are"          "condition"
                                       |
                                  "getting better"
      
      
        ```
        
```
car     ::= make
         |  car ", " make
make ::= "Ford" | "Toyota" | "BMW"
The string "Ford, Toyota, BMW, Toyota, Ford" is in the language because of the following parse tree:

                                 ________ car __________
                                /                \      \
                    _________ car ________        |    make
                   /               \      \       |      |
           ______ car _______       |      make   |      |
          /           \      \      |      |      |      |
     __ car __         |   make     |      |      |      |
    /    |    \        |      |     |      |      |      |
  car    |   make      |      |     |      |      |      |
   |     |      |      |      |     |      |      |      |
make     |      |      |      |     |      |      |      |
   |     |      |      |      |     |      |      |      |
"Ford" " , " "Toyota" ", " "BMW" ", " "Toyota" ", " "Ford"

```
####Grammar for Empty language
`empty ::= `

####Grammar for "olingthi"
- "olingthi" only takes an empty string as the only valid sentence in this language.

 `olingthi ::= ""`
 
- notice the difference between empty language and the empty string.

####Grammar for a letter language

  `letter ::= "a" | "b" | "c" | "d" | ... | "z"`

```
letter ::= "a"
letter ::= "b"
letter ::= "c"
letter ::= "d"
...
letter ::= "z"
```
####Defining a grammar for the word language
  `word ::= letter | word letter`

In this grammar featuring recursive rule, "water" is in this language
- "w" is a word (a sentence in the word language) because it is a letter 
- `word ::= letter`
- "wa" is a word because "w" is a word and "a" is a letter
- `word ::= word letter`
- "wat" is a word because "wa" is a word and "t" is a letter
- "wate" is a word because "wat" is a word and "e" is a letter
- ...

[reference](https://github.com/cs61)

- learn the [shell](https://linuxcommand.org/lc3_learning_the_shell.php)
- Bash Reference [Manual](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
- 
####Interpreter and its environment
- source files are treated as UTF-8 by default
- to change from  default encoding use: `-*- coding: encoding -*-`
- [Argument Passing](https://docs.python.org/3/tutorial/interpreter.html#argument-passing)
- script's name and its arguments are converted into a list and stored in the `argv` variable inside the `sys`
module `sys.argc[]`
- 