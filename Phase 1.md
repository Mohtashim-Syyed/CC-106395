# CC Spring 2021: Project Phase 1 #
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63152** | **Syed Muhammad Mohtashim Kamal**
63433 | Yousuf Muhammad Khan


## Language Selected ##
Mini Pascal

## Function Example ##
```
 function  addition(a, b: integer) : integer;    
       begin      
         addition := a + b;  // this is the return value     
       end;    
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




## Lexical Specification##
IF
ELSE
{    
}
ID := (LETTER|"\_") + (LETTER|"\_"|DIGIT)*
REAL :=

## Language CFG ##

PROG -> LIB FUNCTION | ;
