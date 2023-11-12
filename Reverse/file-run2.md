# file-run2
## Description
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"?

Attached file: run
## Solution
Similar to the previous question, we have to make the file runnable using chmod +x command on linux. To do this, open WSL and navigate to the "mnt" folder from where you can access local files on your PC.

On finding the folder, we can run the commands
```
chmod +x run
./run Hello!
```
which will print out the flag.
## Answer
```
The flag is: picoCTF{F1r57_4rgum3n7_96f2195f}
```