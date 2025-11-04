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

|        1200:12          |    1204:24               |

|        1202:34          |    1205:68               |

|        1202:12          |    1206:00               |

|        1203:34          |    1207:c4               |

#### Manual Calculations
![WhatsApp Image 2025-11-04 at 9 03 09 AM](https://github.com/user-attachments/assets/31971d4c-1ba1-463b-865b-87504ba7a725)


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="627" height="402" alt="addition" src="https://github.com/user-attachments/assets/43231f2b-8320-4cdf-8456-8587b11fc995" />
<img width="629" height="388" alt="addition output" src="https://github.com/user-attachments/assets/18fcf81f-f82b-4402-b962-23196b95a128" />

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
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
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


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1204:00         |
| ----------------------- | ------------------------ |
|          1201:34        |          1205:00         |
| ----------------------- | ------------------------ |
|          1202:12        |          1206:00         |
| ----------------------- | ------------------------ |
|          1203:34        |          1207:C4         |
| ----------------------- | ------------------------ |
#### Manual Calculations

![WhatsApp Image 2025-11-04 at 9 03 10 AM](https://github.com/user-attachments/assets/f4d7ced9-11f6-4cc0-be98-4f7583ae20e0)

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="626" height="398" alt="suptraction" src="https://github.com/user-attachments/assets/7be0ed8e-12e5-4328-a8f7-2e7fbd8a9ae3" />
<img width="631" height="396" alt="sup_output" src="https://github.com/user-attachments/assets/1b7ac2e7-1c97-4ce2-bba6-347b6d54d13a" />

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
|         1200:12         |          1204:44         |
| ----------------------- | ------------------------ |
|          1201:34        |          1205:51         |
| ----------------------- | ------------------------ |
|          1202:12        |          1206:97         |
| ----------------------- | ------------------------ |
|          1203:34        |          1207:0A         |
| ----------------------- | ------------------------ |

#### Manual Calculations

![WhatsApp Image 2025-11-04 at 9 03 10 AM (1)](https://github.com/user-attachments/assets/47efc09d-c72c-4ba5-94e7-75c62580d34c)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="630" height="377" alt="multiplication" src="https://github.com/user-attachments/assets/b0174bdf-4be0-4f5e-8e01-a816812e242b" />
<img width="628" height="386" alt="mull_out" src="https://github.com/user-attachments/assets/141cf8f9-bfff-4c94-b0a1-7c478aff0520" />

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
|         1200:12         |          1204:01         |
| ----------------------- | ------------------------ |
|          1201:34        |          1205:00         |
| ----------------------- | ------------------------ |
|          1202:12        |          1206:00         |
| ----------------------- | ------------------------ |
|          1203:34        |          1207:00         |
| ----------------------- | ------------------------ |
#### Manual Calculations

![WhatsApp Image 2025-11-04 at 9 03 10 AM (2)](https://github.com/user-attachments/assets/fd4c1359-2bb0-4d92-96bd-f9df1043e423)


## OUTPUT FROM MASM SOFTWARE

<img width="635" height="398" alt="division" src="https://github.com/user-attachments/assets/3a81952d-2fec-40b1-8bd8-e0fa6f536dc8" />

<img width="642" height="401" alt="div_out" src="https://github.com/user-attachments/assets/a8425128-6ee5-4ae2-9f66-f0e669cfd11b" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
