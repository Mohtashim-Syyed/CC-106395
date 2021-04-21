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
