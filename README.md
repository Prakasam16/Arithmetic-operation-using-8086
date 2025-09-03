# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200:12                |                  1204:24 |
|  1201:34                |                  1205:68 |
|  1202:12                |                          |
|  1203:34                |                          |

#### Manual Calculations



---![IMG-20250830-WA0002 1](https://github.com/user-attachments/assets/b6bde718-d2b7-4bd3-bdba-87a71beeb31f)


## OUTPUT IMAGE FROM MASM SOFTWARE

![add](https://github.com/user-attachments/assets/fcca764f-747f-4f69-b5c5-d3a6edaadd7d)


![add1](https://github.com/user-attachments/assets/17e614b4-0b0a-4690-a7b5-166329720ab4)






## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,O0H
MOV AX, [SI]
MOV BX, [SI+02H]
SUB AX, BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|    1200:12               |  1204:00                 |
|   1201:34               |  1205:00                 |              
|   1202:12               |                          |
|   1203:34              |                          |

#### Manual Calculations


---![IMG-20250830-WA0001 1](https://github.com/user-attachments/assets/74782ca9-d519-4e36-95b2-9d8630b7a1a0)


## OUTPUT SCREEN FROM MASM SOFTWARE

![sub](https://github.com/user-attachments/assets/4ff0b65c-d7e0-4777-bcc5-79dc66ea543f)



![sub1](https://github.com/user-attachments/assets/a2c53a89-770f-46d0-8797-cd93e6d60c71)




## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200:12              |  1204:44                 |
|   1201:34               |  1205:51                 |              
|   1202:12               |  1206:97                 |
|   1203:34               |  1207:0A                 |

#### Manual Calculations

(Add your calculation here)

---<img width="711" height="576" alt="image" src="https://github.com/user-attachments/assets/59afaac2-8ee4-4a7a-b3e0-a02217a2be28" />

## OUTPUT SCREEN FROM MASM SOFTWARE

![Mul](https://github.com/user-attachments/assets/f8c5cd61-01ae-414b-9b0a-752fadaeb35f)

![mul1](https://github.com/user-attachments/assets/3a0d012a-41a2-4436-930b-8063161f2753)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200:12               |                          |
|   1201:34               |  1204:01                 |              
|   1202:12               |  1205:00                 |
|   1203:34               |  1206:00                 |

#### Manual Calculations



---<img width="738" height="576" alt="image" src="https://github.com/user-attachments/assets/024d6a5c-9956-4ccd-8751-494f3c7ea6dc" />
## OUTPUT FROM MASM SOFTWARE

![div 1](https://github.com/user-attachments/assets/e6313602-cc12-4521-a9b6-db50a42a4f84)


![div](https://github.com/user-attachments/assets/96e18f24-bb9d-4002-a188-243af5e99fb7)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
