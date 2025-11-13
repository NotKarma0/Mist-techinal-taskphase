# Picoctf

## 1. Rail-Fence
A type of transposition cipher is the rail fence cipher, which is described here. Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?
Download the message here.
Put the decoded message in the picoCTF flag format, picoCTF{decoded_message}.

### Solve
**Flag:** `picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_4A76B997}`

I used a rail fence docer. Then i increased the default number of rails from 3 to 4 and i got the flag.


### New Learnings
Rail fence cipher

### References 
None

## 2. Cheese
Try to decrypt the secret cheese password to prove you're not the imposter! Additional details will be available after launching your challenge instance. nc verbal-sleep.picoctf.net 60326.

### Solve
**Flag:** `picoCTF{ChEeSy1c6e2cf3}`

Since the hints gave away that is was a Affine cipher. I knew what i need to do. I typed in cheddar which is a type of cheese which gave out IBARRQN. After comparing and writing equations i get.
2a+b=8, 7a+b=1 where b is mod 26

Upon decrypting it gave SAANENKAESEHQF. Which i entered to guess the code and voila i got the flag.

```bash
nc verbal-sleep.picoctf.net 61023

*******************************************
***             Part 1                  ***
***    The Mystery of the CLONED RAT    ***
*******************************************

The super evil Dr. Lacktoes Inn Tolerant told me he kidnapped my best friend, Squeexy, and replaced him with an evil clone! You look JUST LIKE SQUEEXY, but I'm not sure if you're him or THE CLONE. I've devised a plan to find out if YOU'RE the REAL SQUEEXY! If you're Squeexy, I'll give you the key to the cloning room so you can maul the imposter...

Here's my secret cheese -- if you're Squeexy, you'll be able to guess it:  WQQDADCQAWABEJ
Hint: The cheeses are top secret and limited edition, so they might look different from cheeses you're used to!
Commands: (g)uess my cheese or (e)ncrypt a cheese
What would you like to do?
e

What cheese would you like to encrypt? cheddar
Here's your encrypted cheese:  IBARRQN
Not sure why you want it though...*squeak* - oh well!

I don't wanna talk to you too much if you're some suspicious character and not my BFF Squeexy!
You have 2 more chances to prove yourself to me!

Commands: (g)uess my cheese or (e)ncrypt a cheese
What would you like to do?
g


   _   _
  (q\_/p)
   /. .\.-.....-.     ___,
  =\_t_/=     /  `\  (
    )\ ))__ __\   |___)
   (/-(/`  `nn---'

SQUEAK SQUEAK SQUEAK

         _   _
        (q\_/p)
         /. .\        
  ,__   =\_t_/=   
     )   /   \      
    (   ((   ))   
     \  /\) (/\    
      `-\  Y  /    
         nn^nn        
                          

Is that you, Squeexy? Are you ready to GUESS...MY...CHEEEEEEESE?
Remember, this is my encrypted cheese:  WQQDADCQAWABEJ
So...what's my cheese?
SAANENKAESEHQF

         _   _
        (q\_/p)
         /. .\         __
  ,__   =\_t_/=      .'o O'-.
     )   /   \      / O o_.-`|   
    (   ((   ))    /O_.-'  O |  
     \  /\) (/\    | o   o  o|   
      `-\  Y  /    |o   o O.-`  
         nn^nn     | O _.-'      
                   '--`         

munch...

         _   _
        (q\_/p)
         /. .\         __
  ,__   =\_t_/=      .'o O'-.
     )   /   \      / O o_.-`|   
    (   ((   ))      ).-'  O |  
     \  /\) (/\      )   o  o|   
      `-\  Y  /    |o   o O.-`  
         nn^nn     | O _.-'      
                   '--`         

munch...

         _   _
        (q\_/p)
         /. .\         __
  ,__   =\_t_/=      .'o O'-.
     )   /   \      / O o_.-`|   
    (   ((   ))        )'  O |  
     \  /\) (/\          )  o|   
      `-\  Y  /         ) O.-`  
         nn^nn        ) _.-'      
                   '--`         

MUNCH.............

YUM! MMMMmmmmMMMMmmmMMM!!! Yes...yesssss! That's my cheese!
Here's the password to the cloning room:  picoCTF{ChEeSy1c6e2cf3}
$ nc verbal-sleep.picoctf.net 60326
```

### New Learnings
Affine cipher

### References 
https://en.wikipedia.org/wiki/Affine_cipher
