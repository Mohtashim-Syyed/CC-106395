
# CC Spring 2021: Project Phase 2 #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal**
63433 | Yousuf Muhammad Khan

## Lexical Analyzer ##

Lexical analysis is the first phase of a compiler. It takes the modified source code from
language preprocessors that are written in the form of sentences. The lexical analyzer breaks
these syntaxes into a series of tokens, by removing any whitespace or comments in the source
code.

## Process Flow Diagram Of Lexical Analyzer ##
![Capture](https://user-images.githubusercontent.com/61554600/115705946-9410b480-a386-11eb-8874-693c326d1d2f.PNG)

## Flex Script ##

We have used the lex tool to write a script to generate the Scanner or the Lexical analyser. This
script has three sections as followed,
1. Definition Section
This section is for importing any C header files, variable declarations for variables which
are used later in the program etc.
2. Rules Section
This section is for defining the rules for every token type using regular expressions, the
scanner uses these rules to match lexemes in the test file to various tokens.
3. C Code Section
This section is for C code in the script, here we call functions for setting up the symbol
and the constant table along with displaying them, and calling the lexical analyser using
the yylex() function.
