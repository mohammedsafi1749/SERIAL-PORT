
# Serial Transfer of Single Byte / Character using 8051 (Keil)
## NAME: MOHAMMED SAFI F
## REG NO: 212224060156

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
#include <reg51.h>

void main (void)
{
TMOD = 0X20;
TH1 = 0XFA;
SCON = 0X50;
TR1 =1;
	
SBUF ='A';
while (T1 == 0);
T1=0;
	
while(1);
}
```
### (ii) Serial Port to Transfer a Message

```
#include <reg51.h>

void main(void)
{
    unsigned char msg[] = "VETRI";
    unsigned char i;

    TMOD = 0x20;      // Timer1 Mode2
    TH1  = 0xFD;      // 9600 baud rate
    SCON = 0x50;      // Serial mode1
    TR1  = 1;         // Start Timer1

    for(i = 0; msg[i] != '\0'; i++)
    {
        SBUF = msg[i];
        while(TI == 0);
        TI = 0;
    }

    while(1);
}
```

### OUTPUT:

### (i) Serial Port Transfer a Single Character

<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/25759442-924d-48f4-b060-37386d74fd3d" />

### (ii) Serial Port to Transfer a Message

<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/6ec4afcc-88ca-4508-b48d-caf87a48046b" />

### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
