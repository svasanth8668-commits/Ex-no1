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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200:12           |    1204:24               |
|       1201:34           |    1205:68               |
|       1202:12           |
|       1203:34           |

#### Manual Calculations

<img width="976" height="719" alt="image" src="https://github.com/user-attachments/assets/bd7b147d-9688-44ee-adfa-b89ea73a86cd" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="818" height="549" alt="Screenshot 2026-05-14 at 3 37 48 PM" src="https://github.com/user-attachments/assets/0729d002-8c96-45e2-b813-463fac8d19a6" />


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
|       1200:12           |    1204:00               |
|       1201:34           |    1205:00               |
|       1202:12           |
|       1203:34           |

#### Manual Calculations

<img width="1308" height="729" alt="image" src="https://github.com/user-attachments/assets/574312e8-037b-4f1a-b202-2bdf4566c1b6" />



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="843" height="541" alt="Screenshot 2026-05-14 at 3 44 10 PM" src="https://github.com/user-attachments/assets/5250e5f0-1e18-4c10-bf25-fdc06a6e2739" />


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
|       1200:12           |    1204:00               |
|       1201:34           |    1205:00               |
|       1202:12           |    1206:97               | 
|       1203:34           |    1207:0A               |

#### Manual Calculations

<img width="1439" height="896" alt="image" src="https://github.com/user-attachments/assets/8a879997-a801-4147-9c4c-b86daf83ccf4" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="696" height="268" alt="Screenshot 2026-05-14 at 3 48 04 PM" src="https://github.com/user-attachments/assets/807995b2-0298-4775-aae2-96010d045a23" />


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
|       1200:12           |                          |
|       1201:34           |    1204:01               |
|       1202:12           |    1205:00               | 
|       1203:34           |    1206:00               |


#### Manual Calculations

<img width="1274" height="637" alt="image" src="https://github.com/user-attachments/assets/7e944021-2336-4b72-9690-a68d9b7952a3" />

## OUTPUT FROM MASM SOFTWARE
<img width="862" height="489" alt="Screenshot 2026-05-14 at 3 51 16 PM" src="https://github.com/user-attachments/assets/11b3f8aa-d12e-4b41-b8ee-873e832d6bbc" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

