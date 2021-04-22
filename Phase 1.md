# CC Spring 2021: Project Phase 1 #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal**
63433 | Yousuf Muhammad Khan


## Language Selected ##
Mini C

## Variable Declaratrion Example ##

**Declaration** | **Meaning**
------------ | -------------
int n | n is an integer
int *p| p is a pointer to integer
int a[3]| a is array of 3 integers
int *i[4]| i is array of 4 pointers to integers


## Declaratrion Of Global Function Example ##
```
void swap(int *x, int *y) { ... }
```

## Expressions ##
```
(*p + 1) * 12
```

## Statements ##
```
if (x != 0) y = 1/x;
```

## Function Example ##

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
## For Loop Example ##
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
-Keyword “int,string” 
-Identifier “main” 
-Parentheses “(,)” 
-Open brace ”{“ 
-return keyword “return”
-Constant “2” 
-Semicolon “;”
-Close brace “}”
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
