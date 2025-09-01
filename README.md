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
   1200:12                |   24:1204
   1201:34                |    68:1205
   1202:12                |    00:1206
   1203:34                |   C4:1207                    |                          |

#### Manual Calculations

<img width="634" height="678" alt="image" src="https://github.com/user-attachments/assets/5b6ba9e0-0b7d-4032-ac2d-a175f676a15e" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/6791e711-0a72-41d6-a94f-e1f73161eccf" />
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/91e97e15-07c8-4a7e-ada2-94efb55e86b6" />

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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200:12                |    00:1204
|  1201:34                |    00:1205
   1202:12                |    00:1206
   1203:34                |   C4:1207

#### Manual Calculations

(Add your calculation here)
<img width="634" height="714" alt="image" src="https://github.com/user-attachments/assets/c0b404cf-9f1c-4060-b716-9fac90d1c61a" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/63bd3cb8-8190-4064-b71f-f9652ebf7f03" />
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/6a24f83f-d482-497f-9a7e-91e35ba8a4e0" />

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
|  1200:12                |    44:1204
|  1201:34                |    51:1205
   1202:12                |    97:1206
   1203:34                |   0A:1207                 |                          

#### Manual Calculations

(Add your calculation here)
<img width="725" height="1093" alt="image" src="https://github.com/user-attachments/assets/5460a60d-b6c6-4d16-9050-e4f4efa69821" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/1145660f-9b46-4ad4-94aa-98cd97baf2ba" />
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/e3d9d5d5-56c7-4b31-9e96-51df0d7ef14e" />

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
|  1200:12                |    00:1204
|  1201:34                |    01:1205
   1202:12                |   00:1206
   1203:34                |   00:1207                |                          

#### Manual Calculations

(Add your calculation here)
<img width="550" height="783" alt="image" src="https://github.com/user-attachments/assets/3c995dab-0447-403e-a0fc-b8d526f3c171" />

---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/b39e1251-92ed-4406-a18b-6c6f56dcbbe5" />
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/14a7d8da-20a0-4f4b-ae7e-141eb7b31416" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
