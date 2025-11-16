
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

<img width="936" height="274" alt="511745438-e67ca6f5-8333-41c7-90cc-b74448870955" src="https://github.com/user-attachments/assets/158a418f-8071-4e4c-ae8d-814bd93ae556" />

<BR>
<BR>
<BR>
After execution: D:0x40H:

<img width="985" height="304" alt="511745447-6a839b04-01ce-48be-9408-5851ec4802c9" src="https://github.com/user-attachments/assets/6b7cc883-bfc0-4ac3-b879-7c7890128764" />

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

<img width="950" height="272" alt="511745470-9731ccd1-3b20-4ebb-9f4d-758f800bec64" src="https://github.com/user-attachments/assets/dc221690-4dcb-4876-9514-9e6acf76011d" />

D:0x40H:
<BR>
<BR>
<BR>
<BR>
After execution:

<img width="984" height="291" alt="511745481-3aa084ba-8eda-4a4d-8806-32d0d02e4eb0" src="https://github.com/user-attachments/assets/38d03aca-3088-4d0c-b7d8-3e680b033a27" />


D:0x40H:
<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

