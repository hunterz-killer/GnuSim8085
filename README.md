# GnuSim8085
A Repo of code for Simple Problems coded in Intel 8085 Assembly Language

## Question 1:

Write an assembly program to add the numbers stored in registers B, C and D and save the result in register H.
```
MVI B, 03
MVI C, 03
MVI D, 01
ADD B
ADD C
ADD D
MOV H, A
HLT
```

[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-1)


## Question 2:
Write a program to subtract the value stored in register H from register B and display the result to output port 03(H). Also save the result in register D.
```
MVI B, 07
MVI H, 03
MOV A, B
SUB H
MOV D, A
OUT 03
HLT
```


[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-2)

## Question 3:

Write  a  program  to  read  three  numbers  from  the  input  port  05(H),  add  those numbers  and  save  the  result  in  register  H.  Also  display  the  final  result  on output port 07(H). 
```
MVI B,00
IN 04
MOV B,A
IN 05
MOV C,A
IN 06
MOV D,A
ADD B
ADD C
MOV H,A
OUT 07
HLT
```

[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-3)

## Question 4:

Write a program to find the largest among two numbers stored in registers B and C and display the largest number to port 08(H). 
```
MVI B,04
MVI C,05
MOV A,B
SUB C
JM LARGE
MOV A,B
OUT 08
HLT
LARGE: MOV A,C
OUT 08
HLT 
```

[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-4)

## Question 5:

Write a program to find the smallest among two numbers stored in registers D and E and save the smallest number in register H. 
```
MVI D,04
MVI E,05
MOV A,D
SUB E
JM SMALL
MOV A,E
OUT 08
HLT
SMALL: MOV A,D
OUT 08
HLT 
```

[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-5)

## Question 6:

Write  a  program  to  read  six  numbers  from  input  port  03(H)  and  count  the number of occurrences of the value 04(H) in it. Save the result in register D and also display the result on port 05(H). 
```
MVI H,00
MVI C,06
MVI B,06
IN 04
MOV H,A

IN 03
SUB H
JZ RES1
INR B

RES1: DCR B
IN 03
SUB H
JZ RES2
INR B

RES2: DCR B
IN 03
SUB H
JZ RES3
INR B

RES3: DCR B
IN 03
SUB H
JZ RES4
INR B

RES4: DCR B
IN 03
SUB H
JZ RES5
INR B

RES5: DCR B
IN 03
SUB H
JZ RES6
INR B

RES6: DCR B

MOV A,C
SUB B
MOV D,A
OUT 05
HLT
```

[Solution Link](https://github.com/hunterz-killer/GnuSim8085/blob/Main/Qn-6)

##  
![Made with Love in India](https://madewithlove.org.in/badge.svg)
