# 1. Rail Fence cipher

## What is this cipher?
Its pretty simple honestly. If they give depth 2, just add one more row below the sentence. And alternate the points between first and second row. If they give depth 3, alternated in a series first,second and thrid and then second then first and so on. Read it row-wise. You arrange these like a V shape of diagonals.

## How to figure out if a cipher is a rail cipher?
Just try to make meaningful words whiel adding random letters between each consecutive alphabets. Or use a decoder and brute force with all values.

# Example:
Hello with a depth of 3.

H               o
    e       l   
        l

Now the encoded version of Hello becomes Hoell

# 2. Affine cipher.

## What is this cipher?
This is a cipher involving linear equations, yeah maths. 
So basically per se you have Hello translating to Shirt

Meaning H-S, e-h and so on.
This mapping is basically 7-18, 4-7 and so on. (A=0, B=1, ... Z=25)

We write down 18=7a+b (mod 26)
               7=4a+b (mod 26) 

We get, 11==3a (mod 26)
So we do modular inverse of 3 mod 26.  3*9=27== 1. (mod 26)
No send 3 to other side it becomes 1/3. We then do 11*9==a. Meaning 99-3*26=a. a=21, then u find b. 
And then use a and b in one of the Affine cipher decoders.

# 3.  Hill cipher.

## What is hill cipher?
This is a matrix cipher you can say.

Basically its very hard, but to say simple.
Say you have this formula

(C1,C2,C3) = (P1,P2,P3) (k13,k23, k33) [this is a 3*3 matrix of 9 elements] (mod 26)

Now the key here is the 3*3 matrix. P1,P2,P3 is our message that needs to be encrypted and C1,C2,C3 is after encryption.

For decryption do inverse. 

And what you are doing here is supposed you have a message called Hi guys, ur gonna write it as Hig uys. And then convert it to numbers making 8 9 6  20 24 18.

Its complex yes.
