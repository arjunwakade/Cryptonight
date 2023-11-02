# Play Nice
## Description
Not all ancient ciphers were so bad... The flag is not in standard format. nc mercury.picoctf.net 40742

Attached file: server.py
## Solution
When the given line of code is run on Linux terminal, the following message is displayed:
```
Here is the alphabet: irlgektq8ayfp5zu037nov1m9xbc64shwjd2
Here is the encrypted message: h5a1sqeusdi38obzy0j5h3ift7s2r2
What is the plaintext message?
```
The file given is a clue to the type of encryption used- that is PlayFair. To find the decrypted text, we can use [dCode](https://www.dcode.fr/playfair-cipher) and input the encrypted text and alphabet array. The original text should look something like this:
```
XQYVHTG02JKPLZO8EYHU25KTIP2DKH
```
which is the original text. 
## Answer
Converting to lowercase and typing it into the terminal displays the following message:
```
Congratulations! Here's the flag: 25a0ea7ff711f17bddefe26a6354b2f3
```
