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

<img width="591" height="269" alt="image" src="https://github.com/user-attachments/assets/99836dd0-be46-4ed7-96e7-6010059834ad" />


#### Manual Calculations

<img width="201" height="134" alt="image" src="https://github.com/user-attachments/assets/b590c6f2-f5d8-495d-87e1-1c82ef4aae3d" />




## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="682" height="464" alt="image" src="https://github.com/user-attachments/assets/40f9218c-0d82-43c2-853f-e026c4d013fa" />




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

<img width="606" height="244" alt="image" src="https://github.com/user-attachments/assets/a746e5fd-3e9e-4a96-b744-eb5d1290c907" />


#### Manual Calculations

<img width="269" height="131" alt="image" src="https://github.com/user-attachments/assets/b684a7c0-2585-4e94-b0ee-3cdfb8e3c5cf" />




## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="680" height="462" alt="image" src="https://github.com/user-attachments/assets/e09b1b78-2a10-4449-8f4f-a306d4095086" />




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

<img width="603" height="274" alt="image" src="https://github.com/user-attachments/assets/0d76ed74-ef8a-499f-a2f5-686f10726902" />


#### Manual Calculations

<img width="599" height="305" alt="image" src="https://github.com/user-attachments/assets/f1d2a6ce-07e8-441a-acf9-600d2b927cce" />



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="688" height="467" alt="image" src="https://github.com/user-attachments/assets/8b7bfa75-638a-472b-88c2-b53806a35980" />



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

<img width="606" height="250" alt="image" src="https://github.com/user-attachments/assets/777b3ca3-f98c-478e-8ce7-350f7e309b6a" />


#### Manual Calculations

<img width="313" height="176" alt="image" src="https://github.com/user-attachments/assets/abc5f41f-2ee7-462f-a012-f4825324acc8" />



## OUTPUT FROM MASM SOFTWARE

<img width="684" height="469" alt="image" src="https://github.com/user-attachments/assets/25d50f0d-d07d-43cd-982b-5db2b204a484" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

