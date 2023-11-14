# Fresh Java
## Description
Can you get the flag?
Reverse engineer this Java program.

Attached file: KeygenMe.class
## Solution
After decompiling the .class file to a .java program, it is easy to understand that the program is a multiple if-else if condition where it will check all the characters starting from the back end and output "Invalid key" if any of the characters is wrong.
## Answer
Reading each character from bottom to top, we can get the flag:
```
picoCTF{700l1ng_r3qu1r3d_9332a6be}
```