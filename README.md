## NAME Sandeep S
## REG NO:212223220092
# Vigenere Cipher
Vigenere Cipher using with different key values
# AIM:
To develop a simple C program to implement Vigenere Cipher.
## DESIGN STEPS:
### Step 1:
Design of Vigenere Cipher algorithnm 
### Step 2:
Implementation using C or pyhton code
### Step 3:
Testing algorithm with different key values. 
## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
void main()

{
    char plain[10],cipher[10];
    int key,i,length;
    int result;
    printf("\n Enter the plain text:");
    scanf("%s", plain);
    printf("\n Enter the key value:");
    scanf("%d", &key);
    printf("\n \n \t PLAIN TEXt: %s", plain);
    printf("\n \n \t ENCRYPTED TEXT:");
    for(i=0, length = strlen(plain); i<length; i++)
    {
        
        cipher[i]=plain[i] + key;
        if (isupper(plain[i]) && (cipher[i] > 'Z'))
        cipher[i] = cipher[i] - 26;
        if (islower(plain[i]) && (cipher[i] > 'z'))
        cipher[i] = cipher[i] - 26;
        printf("%c", cipher[i]);

    }
    printf("\n \n \t AFTER DECRYPTION : ");
    for(i=0;i<length;i++)
    {
        
        plain[i]=cipher[i]-key;
        if(isupper(cipher[i])&&(plain[i]<'A'))
        plain[i]=plain[i]+26;
        if(islower(cipher[i])&&(plain[i]<'a'))
        plain[i]=plain[i]+26;
        printf("%c",plain[i]);
    }

    
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/cafdb0b5-caf7-48b9-a5bf-3d0712776853)

## RESULT:
The program is executed successfully
