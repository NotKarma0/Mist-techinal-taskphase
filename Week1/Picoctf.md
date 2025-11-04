# Picoctf

## 1. Interencdec
Can you get the real meaning from this file. Download the file here.

### Solve
**Flag:** `picoCTF{caesar_d3cr9pt3d_ea60e00b}`

So when i did cat enc_flag. It showed me gibberish. Since its ending with == and also has only alphabets and numbers I understood that its a base64 encoded code. Now when i decoded it. It showed me a similar kind of text once again ending with ==' and starting with b'.. So i removed the first and last parts and decoded it again. It gave me this. 
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}
I put it in the cipher identified and finally understood that it may be ceaser cipher. When i decoded it with ceaser cipher. It gave me the final flag.

```bash
:~/Desktop/hack$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==
:~/Desktop/hack$ ^C
:~/Desktop/hack$ echo 'YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyeG9OakJzTURCcGZRPT0nCg==' |base64 --decode
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ=='
:~/Desktop/hack$ echo 'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ==' |base64 --decode
wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}
```

### New Learnings
I learned how to identify if a code is base 64. And how to identify different ciphers.

### References 
https://www.dcode.fr/cipher-identifier
https://www.dcode.fr/caesar-cipher

## 2. Mod 26
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_GYpXOHqX}

### Solve
**Flag:** `picoCTF{next_time_I'll_try_2_rounds_of_rot13_TLcKBUdK}`

Basically rot 13. Transfers every alphabet by 13 characters. So I used a website which decodes the given flag for the actual flag.

### New Learnings
None

### References 
https://cryptii.com/pipes/rot13-decoder


## 2. 13
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}

### Solve
**Flag:** `picoCTF{not_too_bad_of_a_problem}`

Same as before.

### New Learnings
None

### References 
https://cryptii.com/pipes/rot13-decoder
