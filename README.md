
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="953" height="281" alt="image" src="https://github.com/user-attachments/assets/a17e4350-203a-48ab-bcc2-a5de0c36b85c" />

<BR>
<BR>
<BR>
After execution: D:0x40H:
<img width="959" height="298" alt="image" src="https://github.com/user-attachments/assets/3331efdd-c5b8-43ff-846e-54c85a9f2538" />

<BR>
<BR>
<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
<img width="959" height="271" alt="image" src="https://github.com/user-attachments/assets/db79a0ac-33ee-4878-9acc-38db6305ed17" />

D:0x40H:
<BR>
<BR>
<BR>
<BR>
After execution:
<img width="961" height="274" alt="image" src="https://github.com/user-attachments/assets/424bf580-f47d-47e4-b6b4-43566ea8d055" />

D:0x40H:
<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

