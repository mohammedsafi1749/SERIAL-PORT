# Transfer single byte / character serially using 8051 KEIL.(EMBEDDED C Program)

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
    unsigned char msg[] = "SAFI";
    unsigned char i;

    TMOD = 0X20;  
    TH1  = 0XFA;
    SCON = 0X50;      
    TR1  = 1;

    for(i = 0; i<=12; i++)
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

<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/13406ff3-cf5c-46bd-9fca-56c2446f53bf" />

### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
