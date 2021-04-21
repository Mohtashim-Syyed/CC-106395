# CC Spring 2021: Project Phase 1 #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal**
63433 | Yousuf Muhammad Khan


## Language Selected ##
Mini Pascal

## Variable Declaratrion Example ##
```
VAR Sum, Number: INTEGER; 
```

## IF ELSE Example ##
```

PROGRAM FindLarge;
 { THIS PROGRAM READS IN TWO INTEGERS. IT
 WILL DETERMINE WHICH IS THE LARGER OF THE TWO,
 AND PRINT AN APPROPRIATE MESSAGE }
 VAR
 Number1:INTEGER;{FIRST NUMBER READ}
 Number2:INTEGER;{SECOND NUMBER READ}
 Larger:INTEGER;{THE LARGER ONE}
 BEGIN
 READLN(Number1,Number2);
 IF Number1 > Number2 THEN
 Larger := Number1
 ELSE
 Larger := Number2;
 WRITELN('THE LARGER OF ',Number1,
 ' AND ',Number2,' IS ',Larger)
 END. 
 ```
## Function Example ##
```
 function  addition(a, b: integer) : integer;    
       begin      
         addition := a + b;  // this is the return value     
       end;    
```

## Procedure Example ##
```
PROCEDURE PrintGraph (Size:INTEGER);
 {PROCEDURE TO OUTPUT A LINE OF 'SIZE' ASTERISKS}
 VAR
 I:INTEGER;
 BEGIN
 FOR I:=1 TO Size DO
 WRITE('*');
 WRITELN
 END; 

```
## Array Example ##
```
  VAR a, b : array [ 1 .. 10 ] of array [ 1 .. 10 ] of Integer;
    a[5] := b[3];    
```
## For Loop Example ##
```
 for i:= 1 to 10 do writeln(i);
 
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
"begin" | "end" | "var" | "array" | "procedure" |
"function" | "program" | "assert"
<predefined id> ::= "Boolean" | "false" | "integer" | "read" | "real" | "size" | "string" | "true" | "writeln" 
```
## Language CFG ##
```
<program> ::= "program" <id> ";" <block> "."
<declaration> ::= "var" <id> { , <id> } ":" <type> |
"procedure" <id> "(" parameters ")" ";" <block> |
"function" <id> "(" parameters ")" ":" <type> ";" <block>
<parameters> ::= [ "var" ] <id> ":" <type> { "," [ "var" ] <id> ":" <type> } | <empty>
<type> ::= <simple type> | <array type>
<array type> ::= "array" "[" [<integer expr>] "]" "of" <simple type>
<simple type> ::= <type id>
<block> ::= "begin" <statement> { ";" <statement> } [ ";" ] "end"
<statement> ::= <simple statement> | <structured statement> | <declaration>
<empty> ::=
<simple statement> ::= <assignment statement> | <call> | <return statement> |
< read statement> | <write statement> | <assert statement>
<assignment statement> ::= <variable> ":=" <expr>
<call> ::= <id> "(" <arguments> ")"
<arguments> ::= expr { "," expr } | <empty>
<return statement> ::= "return" [ expr ]
<read statement> ::= "read" "(" <variable> { "," <variable> } ")"
<write statement> ::= "writeln" "(" <arguments> ")"
<assert statement> ::= "assert" "(" <Boolean expr> ")"
<structured statement> ::= <block> | <if statement> | <while statement>
<if statement> ::= "if" <Boolean expr> "then" <statement> |
"if" <Boolean expr> "then" <statement> "else" <statement>
<while statement> ::= "while" <Boolean expr> "do" <statement> 
<expr> ::= <simple expr> |
<simple expr> <relational operator> <simple expr>
<simple expr> ::= [ <sign> ] <term> { <adding operator> <term> }
<term> ::= <factor> { <multiplying operator> <factor> }
<factor> ::= <call> | <variable> | <literal> | "(" <expr> ")" | "not" <factor> | < factor> "." "size"
<variable> ::= <variable id> [ "[" <integer expr> "]" ]
<relational operator> ::= "=" | "<>" | "<" | "<=" | ">=" | ">"
<sign> ::= "+" | "-"
<adding operator> ::= "+" | "-" | "or"
<multiplying operator> ::= "*" | "/" | "%" | "and" 
 ```
