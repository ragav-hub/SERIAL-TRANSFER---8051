# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}
```
**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h> void main(void)

{

unsigned char msg[]="8051 MICROCONTROLLER"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<25;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}
```
 
**OUTPUT:**

Serial port transfer a character A:
<img width="1039" height="174" alt="image" src="https://github.com/user-attachments/assets/aec974d6-4c17-4775-8e8a-f14211e5ba8c" />

Serial port to Transfer a Message:
<img width="955" height="277" alt="image" src="https://github.com/user-attachments/assets/89597ed9-57e7-464c-877a-0c41ee6f4407" />


<br>
<br>
<br>
<br>
<br>

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
