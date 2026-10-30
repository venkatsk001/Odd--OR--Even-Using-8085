## Aim:
To write an 8085 microprocessor program to check whether a given 8-bit number is odd or even.
## Apparatus Required:
Laptop with an internet connection
## Algorithm:
1.	Load the number from a specified memory location into register A.
2.	Perform an AND operation with 01H to check the least significant bit (LSB).
3.	If the result is 0, the number is even; otherwise, it is odd.
4.	Store the result in a specific memory location (odd or even flag).
## Program:
; Program: Check Odd or Even
; Input  : Number is stored at 2050H
; Output : If number is even -> 01 stored at 2051H
;          If number is odd  -> 00 stored at 2051H

LDA 2050H       ; Load number from memory into accumulator
ANI 01H         ; Mask all bits except LSB (A = A AND 01H)
JZ EVEN         ; If Zero Flag = 1 → Number is even

; If odd
MVI A,00H       ; Load 00 into accumulator
STA 2051H       ; Store result (Odd)
HLT             ; Stop program

EVEN: 
MVI A,01H       ; Load 01 into accumulator
STA 2051H       ; Store result (Even)
HLT             ; Stop program
## Output:
<img width="817" height="471" alt="image" src="https://github.com/user-attachments/assets/60a8c406-b36a-4809-afa0-28eea8d34254" />
<img width="822" height="458" alt="Screenshot 2026-10-30 143920" src="https://github.com/user-attachments/assets/0154d993-0cfd-4ae7-8c29-7b30b2eed699" />

## Result:
The 8085 microprocessor successfully checks whether a given number is odd or even and stores the result in memory.


