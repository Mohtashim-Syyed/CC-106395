# CC Spring 2021: Project Phase 3 #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal**
63433 | Yousuf Muhammad Khan

## Parser ##
A parser is a compiler or interpreter component that breaks data into smaller
elements for easy translation into another language. A parser takes input in the form
of a sequence of tokens or program instructions and usually builds a data structure
in the form of a parse tree or an abstract syntax tree.

## Parser Interacting With Lexical Analyzer ##

![parser](https://user-images.githubusercontent.com/61554600/115813901-84887e80-a40d-11eb-8776-1f8aa1ce5395.jpg)

## YACC Script ##   

Yacc stands for Yet Another Compiler-Compiler. Yacc provides a general tool for
describing the input to a computer program. The Yacc user specifies the structures
of his input, together with code to be invoked as each such structure is recognized.  

The structure of our Yacc script is given below; Our file is divided into three sections which are as follows:    

- Definition section      
      
- Rules section    

- C code section     

The definition section is used to define any parameters for the C program, any
header files to be included and global variable declarations. We also define all
parameters related to the parser here, specifications like using Leftmost derivationsor Rightmost derivations, precedence and left right associativity are declared here,
data types and tokens which will be used by the lexical analyser are also declared here.   

The Rules section contains the entire grammar which is used for deciding if the input
text is legally correct according to the specifications of the language. Yacc uses this
rules for reducing the token stream received from the lexical Analyzer, all rules are linked to
each other from the start state, which is declared in the rules section.    

In the C code section the parser is called, and the symbol table and constant tables
are initialised in this section. The lex.yy.c file created by the lex script is also included
from here which the parser calls. In this section we also define the error function
used by the parser to report syntactical errors along with line numbers.

## REFERENCES ##

- Parser Introduction: 
- Parser Interacting With Lexical Analyzer: https://www.brainkart.com/article/Lexical-Analysis_8074/ 
