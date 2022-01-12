##Why?
Because I wanted to learn...without having to rush the process. <br>

This is my treasure I'm willing to share. I have included all the references for the material used here so feel free to go dig deeper and find out why your code does what it does.
The biggest challenge we have today is finding the balance between chasing the money and producing real quality material for consumption. if you want to learn, you are going to have to find that balance and dig deeper to find meaning in what you do and what is really happening under the hood.

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
- to change from  default encoding use: `-*- coding: encoding -*-` replacing 'encoding' with one of the valid [codecs](https://docs.python.org/3/library/codecs.html#standard-encodings)
- [Argument Passing](https://docs.python.org/3/tutorial/interpreter.html#argument-passing)
- script's name and its arguments are converted into a list and stored in the `argv` variable inside the `sys`
module `sys.argc[]`

####Objects:
- used for data abstraction in Python
- abstraction is used as a productivity enhancer
####Von Neumann model
- Is a form of computer organization based on the stored-program concept, it comprises the following components:
  - memory
  - CPU
  - Input
  - Output
  - Control unit
- Computer systems are organized as systemic set of transformations that brings a problem described in human language to the transistors that actually execute it.
  - you have a problem statement that explains what the issue is.
  - You then transform that into an algorithm
    - Procedural steps that ensure/guarantee precise execution by a computer.
    - The procedure must eventually terminate.
  - Algorithm is transformed into a computer program
  - ISA is the instruction set architecture available in every computer. It is a list of all instruction that a computer can execute and different computers might have different ISA. An example of ISA is x86.
  - A high level programming language such as Python is translated into specific ISA using a translating program called a compiler.
  - Low level programs written in low-level computer specif assembly language is translated using assembler
- Micro-architecture or the microprocessor architecture is a specific implementation if ISA in a given processor depending on the intended goals. For instance the x86 has been implemented slightly differently in Intel and AMD.
- List of Intel CPU [microarchitectures](https://en.wikipedia.org/wiki/List_of_Intel_CPU_microarchitectures)
- List of AMD [microarchitectures](https://en.wikichip.org/wiki/amd/microarchitectures)

At the root of the microarchitecture is the simple [logic circuit](https://circuitverse.org/simulator). You can learn more about logic gates [here](https://www.electronics-tutorials.ws/logic/logic_1.html)

It is also helpful to be have some knowledge of [binary numbers](https://www.electronics-tutorials.ws/binary/bin_1.html) and other [digital circuit Number Systems](https://drive.google.com/file/d/19G_eiyZ9HarpjZPlEYui4TGyVu4Ol_D1/view?usp=sharing)

AND `output = input1 ∧ input2` both are true
OR  `output = input1 ∨ input2` one or both are true

NOT `output = ∼ input1` the output is opposite of the input

![alt oneGate.png](img/oneGate.PNG)
<br>

![alt twoGateSeries](img/twoGateSeries.PNG)
<br> 

![alt twoGatesparallel](img/twoGateParallel.PNG)
<br>

![alt threeGatesParallelAndSeries](img/threeGatesParallelAndSeries.PNG)
<br>

![alt Circuit1](img/Circuit-1.PNG)
<br>

![alt Circuit2](img/Circuit-2.PNG)
<br>

![alt AND](img/AND.PNG) AND `output = input1 ∧ input2` both are true
<br>

![alt OR](img/OR.PNG) OR  `output = input1 ∨ input2` one or both are true
<br>

![alt NOT](img/NOT.PNG) NOT `output = ∼ input1` the output is opposite of the input.
<br>

#Libraries
###Machine learning
- [Scikit-Learn]()
- [TensorFlow]()
- [Pytorch]()
- [Theano]()
<br>

### Web Development
- [Django]()
- [Flask]()
- [Bottle]()
- [Web2py]()
- [Pyramid]()
- [FastAPI]()
<br>

###Ethical Hacking
- [IMPacket]()
- [Cryptography]()
- [Scapy]()
- [pwntools]()
- [Nmap]()
<br>

###Scraping
- [Scrapy]()
- [BeautifulSoup]()
- [Selenium]()
- [Requests]()
- [PyRobot]()
- [Newspaper3k]()
<br>

###Game Development
- [Pygame]()
- [Pyglet]()
- [Cocos2d]()
- [panda3D]()
<br>

###Image Processing
- [Pillow]()
- [Scikit-Image]()
- [OpenCV]()
- [Pytesseract]()
<br>

###Mobile Development
- [Kivy]()
- [BeeWare]()
<br>

###Data Science
- [Scikit-Learn]()
- [Theano]()
- [Scipy]()
- [Numpy]()
- [Pandas]()
- [Scrapy]()
<br>

###Desktop Applications
- [wxPython]()
- [PyQT5]()
- [Pyside]()
- [PySimpleGUI]()
<br>

###BioInformatics
- [BioPython]()
- [Prody]()
- [SciKit-Bio]()
- [Pyensembl]()
- [PySB]()
<br>

###Mathematics and Computation
- [Theano]()
- [Scipy]()
- [Numpy]()
- [Statsmodels]()
- [CuPy]()
- [SymPy]()
<br>

###Testing and Automation
- [Robotframework]()
- [Automate]()
- [Pytest]()
- [Nose]()
- []()
<br>

###Astronomy
- [SpacePy]()
- [Astropy]()
- [SunPy]()
<br>

###Data Visualization
- [Matplotlib]()
- [Seaborn]()
- [Plotly]()
- [Bokeh]()
- [Pydot]()
<br>

###Robotics
- [RobotFramework]()
- [Pydy]()
- [PyBotics]()
<br>

###Cryptocurrency
- [BitCoinLib]()
- [CCXT]()
<br>

###Data Mining
- [Scrapy]()
- [BeautifulSoup]()
- [Selenium]()
<br>

###Computer Vision
- [OpenCV]()
- [Mahotas]()
- [SimpleCV]()
<br>

###Quantum Computing
  - [QuTiP]()
  - [PyQuil]()
  - [Cirq]()
  - [Qiskit](https://qiskit.org/)
<br>
  
###Statistical Computation
- [Pandas](https://pandas.pydata.org/)
- [Statsmodels](https://www.statsmodels.org/stable/index.html)
<br>

###Command Line Applications
- [Typer](https://typer.tiangolo.com/tutorial/first-steps/)
- [cmd2](https://cmd2.readthedocs.io/en/stable/)
- [Click](https://click.palletsprojects.com/en/7.x/)
<br>

###Signal Processing
- [Scipy](https://docs.scipy.org/doc/scipy/reference/tutorial/index.html)
- [PyWavelets](https://pywavelets.readthedocs.io/en/latest/)
<br>

###Interactive Computing
- [IPython](https://ipython.org/)
- [Jupyter Notebook](https://jupyter.org/)
<br>

###Deep Learning
- [TensorFlow](https://www.tensorflow.org/learn)
- [PyTorch](https://pytorch.org/)
- [Keras](https://keras.io/)
- [Chainer](https://chainer.org/)
<br>

###Geographic Processing
- [GeoPandas](https://geopandas.org/en/stable/)
- [Shapely](https://shapely.readthedocs.io/en/stable/project.html)
<br>

###Sciences
- [Scipy](https://scipy.org/)
- [Statsmodels](https://www.statsmodels.org/stable/index.html)
- [CuPy](https://cupy.dev/)
- [PsychoPy](https://www.psychopy.org/)
<br>

###Natural Language Processing
- [NLTK](https://www.nltk.org/)
- [TextBlob](https://pypi.org/project/textblob/)
- [Stanza](https://stanfordnlp.github.io/stanza/)
- [spaCY](https://spacy.io/)
- [Gensim](https://pypi.org/project/gensim/)
<br>

###Cybersecurity
- [IMPacket](https://www.kali.org/tools/impacket/)
- [Cryptography](https://cryptography.io/en/latest/)
- [Scrapy](https://pypi.org/project/Scrapy3/)
- [Twisted](https://pypi.org/project/Twisted/)
- [Faker](https://faker.readthedocs.io/en/master/)

- 