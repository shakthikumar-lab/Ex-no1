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
|       1200   :   12     |     1204     :        24 |
|       1201   :   34     |     1205     :        68 |
|       1202   :   12     |                          |
|       1203   :   34     |                          |

#### Manual Calculations
<img width="2160" height="3840" alt="add" src="https://github.com/user-attachments/assets/4758ae82-6fa0-44b0-b6eb-b2974b9a4b3d" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="640" height="232" alt="add" src="https://github.com/user-attachments/assets/cc1150fc-655a-4e47-9d69-60fe137e4e5a" />


---


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
|       1200   :   12     |     1204     :        00 |
|       1201   :   34     |     1205     :        00 |
|       1202   :   12     |                          |
|       1203   :   34     |                          |

#### Manual Calculations


<img width="2160" height="3840" alt="sub" src="https://github.com/user-attachments/assets/176cabcf-b000-4a8f-9f21-addd29d36796" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="645" height="220" alt="sub" src="https://github.com/user-attachments/assets/c22099f1-231a-4be4-a7d9-cc3e9150adb4" />


---

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
|       1200   :   12     |     1204     :        44 |
|       1201   :   34     |     1205     :        51 |
|       1202   :   12     |     1206     :        97 |
|       1203   :   34     |     1207     :        0A |

#### Manual Calculations

<img width="2160" height="3840" alt="mul" src="https://github.com/user-attachments/assets/8d5bdfb3-2378-4d95-b826-a757258f17c9" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="242" alt="mul" src="https://github.com/user-attachments/assets/d2c61c7e-7fd2-4d8d-ae3c-23b31863eef2" />

---

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
|       1200   :   12     |     1204     :        01 |
|       1201   :   34     |     1205     :        00 |
|       1202   :   12     |     1206     :        00 |
|       1203   :   34     |                          |

#### Manual Calculations

<img width="2160" height="3840" alt="div" src="https://github.com/user-attachments/assets/4457c4f0-de97-48e4-8ee6-74897980d35d" />

---
## OUTPUT FROM MASM SOFTWARE

<img width="646" height="238" alt="div" src="https://github.com/user-attachments/assets/696e4235-842e-417f-b96f-c49943220414" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

===
