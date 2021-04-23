# CC 106395:Mini C #

### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim kamal** <!--this is the group leader in bold-->
63433 | Yousuf Muhammad Khan
<!-- Replace name and student ids with acutal group member names and ids-->
**Mini** C is both a subset of the C programming language, suitable for resource-limited microcomputers and embedded systems, and an implementation of that subset. Originally valuable as an early compiler for microcomputer systems available during the late 1970s and early 1980s, the implementation has also been useful as an example simple enough for teaching purposes.

## Sample Constructs Of The Language ##

### Variable Declaratrion ##

**Declaration** | **Meaning**
------------ | -------------
int n | n is an integer
int *p| p is a pointer to integer
int a[3]| a is array of 3 integers
int *i[4]| i is array of 4 pointers to integers


### Declaratrion Of Global Function ##
```
void swap(int *x, int *y) { ... }
```

### Expressions ##
```
(*p + 1) * 12
```
### Statements ##
```
if (x != 0) y = 1/x;
```

### Function ##

**Calculating Factorial**
```
void main(int i) {
int r;
fac(i, &r);
print r;
}
void fac(int n, int *res) {
if (n == 0)
*res = 1;
else {
int tmp;
fac(n-1, &tmp);
*res = tmp * n;
}
}  
```
### For Loop ##
```
int main() {
  int i;
  for (i = 1; i < 11; ++i)
  {
    printf("%d ", i);
  }
  return 0;
}
 
```

## Lexical Specification ##
```
<id> ::= <letter> { <letter> | <digit> | "_" }
<literal> ::= <integer literal> | <real literal> | <string literal>
<integer literal> ::= <digits>
<digits> ::= <digit> { <digit> }
<real literal> ::= <digits> "." <digits> [ "e" [ <sign> ] <digits>]
<string literal> ::= "\"" { < a char or escape char > } "\""
<letter> ::= a | b | c | d | e | f | g | h | i | j | k | l | m | n | o |
p | q | r | s | t | u | v | w | x | y | z | A | B | C |
D | E | F | G | H | I | J | K | L | M | N | O | P
| Q | R | S | T | U | V | W | X | Y | Z
<digit> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
<special symbol or keyword> ::= "+" | "-" | "*" | "%" | "=" | "<>" | "<" | ">" | "<=" | ">=" |
"(" | ")" | "[" | "]" | ":=" | "." | "," | ";" | ":" | "or" |
"and" | "not" | "if" | "then" | "else" | "of" | "while" | "do" |
"begin" | "end" | "var" | "array"
<predefined id> ::= "Boolean" | "false" | "integer" | "read" | "real" | "size" | "string" | "true" | "printf" | "scanf"

```
## Language CFG ##

```
program = statement*
statement = block
          | SEMI
          | assignment
          | declaration
          | if
          | while
          | 'break' SEMI
          | 'continue' SEMI
          | 'exit' '(' ')' SEMI
          | 'print' parExpression SEMI
          | 'println' parExpression SEMI
block = '{' statement* '}'
expression = literal
           | ID
           | ('!' | '-') expression
           | expression ('*' | '/' | '%') expression
           | expression ('+' | '-') expression
           | expression ('<' | '>' | '<=' | '>=') expression
           | expression ('==' | '!=') expression
           | expression ('&&') expression
           | expression ('||') expression
           | parExpression
           | 'readInt' '(' ')'
           | 'readDouble' '(' ')'
           | 'readLine' '(' ')'
           | 'toString' parExpression
parExpression = '(' expression ')'
assignment = ID assignmentOp expression SEMI
declaration = type ID (assignmentOp expression)? SEMI
if = 'if' parExpression statement ('else' statement)?
while = 'while' parExpression statement
assignmentOp = '='
type = 'int'
     | 'double'
     | 'bool'
     | 'string'
literal = IntegerLiteral
        | FloatingPointLiteral
        | StringLiteral
        | BooleanLiteral
IntegerLiteral = DIGIT+
FloatingPointLiteral = DIGIT+ '.' DIGIT+
StringLiteral = '"' (CHAR | '\"')* '"'
BooleanLiteral = 'true' | 'false'
SEMI = ';'
ID = (LETTER | '_') (LETTER | DIGIT | '_')*
DIGIT = '0' | ... | '9'
LETTER = 'a' | ... | 'z' | 'A' | ... | 'Z'
CHAR = <unicode character, as in Java>
Whitespace characters (' ', '\t', '\r', '\n') are skipped outside of tokens. 
 ```

### Approach ###
-  Flex
-  Yacc
-  Linux Operating Environment

##Problems Faced##
Replace this text with the explaination of the problems you faced in the project, and how you resolved them. Again you can give each of your problems a heading of level 3.

###Problem 1: I don't know how to Code###
Transfer yourself to social sciences department. Blah blah blah. This is an example. Replace it with your own problem description and how you resolved it.
Don't just blindly copy paste this report. This is a sample template file.


## REFERENCES ##

- Mini C Introduction: https://en.wikipedia.org/wiki/Small-C
- Sample Constructs Of The Language: https://homepage.cs.uiowa.edu/~tinelli/classes/3820/Fall16/notes/chap7-micro-C.pdf
- Lexical Analyzer Introduction: https://github.com/gauribaraskar/Mini-C-compiler/blob/master/Report/Report%20-%20Lexical%20Analysis.pdf
