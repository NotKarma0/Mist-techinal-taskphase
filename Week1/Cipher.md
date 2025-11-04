# 1. Base64

## How to identify a base64 cipher:
Base64 cipher can be identified if a encoded message ends with == (or) =. It also almost consits of mix of uppercase and lowercase alphabets, numbers, and the symbols + (or) /.

## How to encrypt your message using base64:
We use this command to encrypt
```bash
:~$ echo 'Hello World' |base64 
SGVsbG8gV29ybGQK
:~$ echo 'SGVsbG8gV29ybGQK' | base64 --decode
Hello World
:~$ 
```
This is how we encrypt and decrypt using the terminal.

# 2. Ceaser cipher

## What exactly is ceaser cipher?
Ceaser cipher is basically a cipher in which you have a sentence. And each and every letter in our alphabets are shifted by a constant k. Now this can be shifted left or right. If its a left shift, every alphabet gets shifted by k constants to the right. And vice verse. 
Example:
If the cipher is left shifted with 2. The letter C would become A, and the letter A would become Y and so on.
If the cipher is right shifted with 2. The letter A would become C, and the letter C would become E and so on.

## How to decrypt ceaser cipher?
I would recommend using this.
https://www.dcode.fr/caesar-cipher

# 3. Vignere cipher
Vignere cipher is basically Ceaser cipher but with like varying constant. Now since we need like the pattern of how the constant is varying, we use another sentence and compare the both. Now if the key used has less number of letters than the initial sentecnce, we compare the next letter in the original sentence to the first letter of the key and it keeps repeating.

Example: 
Basically suppose the sentence is hello world and the key is abcdefghij
Now here what happens is 
hello world is compared with abcdefghij. Now the key is converted to numbers so it becomes 1,2,3,4,5,6,7,8,9,10
Now ceaser cipher is applied. h is shifted by 1 letter. e is shifted by 2. w is shifted by 6 and so on. And yes this is a right shifted cipher. 

## How to decrypt vignere cipher?
I would recommend using this.
https://cryptii.com/pipes/vigenere-cipher

