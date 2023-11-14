# vault-door-3
## Description
This vault uses for-loops and byte arrays. The source code for this vault is here:

Attached file: VaultDoor3.java
## Solution
On opening the file, we can see a Java program to check for a password, and upon entering the right code, will print "Access granted".

The checking function seems to shuffle the characters in the String "jU5t_a_sna_3lpm12g94c_u_4_m7ra41" to create the actual flag String. So, to solve this, I made a function that reversed that process and printed out the expected String input.
```
public void reverse() {
        String password = "jU5t_a_sna_3lpm12g94c_u_4_m7ra41";
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        System.out.println(s);
    }
```
## Answer
The flag is now printed before calling the function checkPassword, and displays
```
jU5t_a_s1mpl3_an4gr4m_4_u_c79a21
```
So the flag is
```
picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}
```