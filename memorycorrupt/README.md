![Alt text](image.png)

## Intro To Buffer Overflow Via Game And Simulation

I found this game in event Advent Cyber 2023 Try Hack Me

## What's You Learn In This Game
How Manipulation Game Using Buffer Overflow to Make coins so big and Manipulation Memory to Win and Get The FLAG

## Start Game
![Alt text](image-1.png)

![Alt text](image-2.png)

## Play and Undesrtanding How Game Work
![Alt text](image-3.png)

So if you walk to green character you can give a name, one abjad you purchase a 1 coins. 

![Alt text](image-4.png)

If you walk to blue character you can buy all item available using code.

![Alt text](image-5.png)

If you walk to tree, you can get the flag, but you should buy d(symbol) item

## IDEA
There is a two question

![Alt text](image-6.png)

![Alt text](image-7.png)

Question 1 no need Game Interaction (so very easy)
Question 2 Need Buffer Overflow

## SOLVE

### QUESTION 1
![Alt text](image-15.png)

### QUESTION 2
In this case game, input name is Buffer Overflow Vuln

![Alt text](image-8.png)

My idea is, overwrite the coins so that, my coins is big let's try. If you look this, you need 12 JUNK and 4 byte to overwrite the coins. First Let's SPC the comp tu get a point, every one SPC you get 1 coins. Need 16 SPC.

![Alt text](image-9.png)

DDDD for ovewrite the coins, let's the result

Problem : i cannot buy d items cuz the blue character says, this unwin game, so imposibble to buy d item, so my idea is overwrite the inv_items using symbols shop need start (d).

![Alt text](image-10.png)

BOOM !.

so now you can custom name buffer overflow for change inv_items to d (need to get flag).

After calculate, i need 44 JUNK and character d in the last (so total is 45)

let's BOF the name

![Alt text](image-11.png)

After BOF, let's go to tree

![Alt text](image-12.png)

Boom

![Alt text](image-13.png)

![Alt text](image-14.png)