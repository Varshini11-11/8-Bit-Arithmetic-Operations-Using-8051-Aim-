# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```



## Output:

<img width="1920" height="1200" alt="Screenshot 2026-03-16 103551" src="https://github.com/user-attachments/assets/74420789-8bc9-4a8f-81b6-dac7f56dd9ea" />

<img width="252" height="489" alt="Screenshot 2026-03-16 103605" src="https://github.com/user-attachments/assets/cf98ec2e-f790-4a8b-b0e6-cf417d899058" />


  
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
ORG 000H
MOV A, 30H
SUBB A, 31H
MOV 40H, A
JNC NEXT
MOV 41H,#01H;
SJMP END_PROGRAM;
NEXT:MOV 41H,#00H;
END_PROGRAM:NOP;
END
```



## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-16 104718" src="https://github.com/user-attachments/assets/1859ed76-0442-4c0a-a052-c447be8f1151" />
<img width="243" height="448" alt="Screenshot 2026-03-16 104735" src="https://github.com/user-attachments/assets/7b2e5e53-3f2f-46ee-9363-a3af857d94fe" />


## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```



## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-16 110128" src="https://github.com/user-attachments/assets/4f00a9f6-d8ed-4db3-a540-0fc744af16b4" />
<img width="230" height="460" alt="Screenshot 2026-03-16 110153" src="https://github.com/user-attachments/assets/67b54c71-7c90-4d92-9cae-ab4d5f3b5cec" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```



## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-16 111120" src="https://github.com/user-attachments/assets/6a870687-85d8-4097-a19b-217844957466" />
<img width="243" height="469" alt="Screenshot 2026-03-16 111139" src="https://github.com/user-attachments/assets/d37c5b8b-0997-4ab2-bd1c-294397914459" />



## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

