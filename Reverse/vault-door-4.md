# vault-door-4
## Description
This vault uses ASCII encoding for the password. The source code for this vault is here:

Attached file: VaultDoor4.java
## Solution
On opening the file, there is a checkPassword method that checks if the byte value of the input password equals to the byte array password.

To reverse this, I added the following lines to the main method before the program asks for input:
```
byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0146, 064 ,
            'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' ,
        };
        String s = new String(myBytes);
        System.out.println(s);
```
## Answer
The code converts the byte array to String and prints it as
```
jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e
```
So the flag is
```
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}
```