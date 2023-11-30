# CSE 280 Prove 12

(c) BYU-Idaho - It is an honor code violation to post this
file completed or uncompleted in a public file sharing site.

**Instructions**: Answer each question using proper markdown notation as needed.  Use the preview view in Visual Studio Code (or another editor if desired) to see the formatting, tables, and mathematical formula properly rendered.  If you need to write code, then first test your code in a separate file and then copy the code into this document using code fences. 

**Name**: Geoffrey Collins

**Section**: 02

**Teacher**: Brother Macbeth

## Question 1 (3 points)

Tessie and her friends have between them 15 board games, 12 card games, and 1 word game.  If their game nights feature the word game plus one other game (either a board game or a card game), how many different game nights can they have?

**Answer**: 180

## Question 2 (3 points)

Now Tessie and her friends have acquired two more word games (for a total of 3) and have deided to vary the snacks they munch on while playing games.  They have selected 7 different types of snacks.  If a game-night configuration consists of a word game, another game (either a board or card game), and a snack, then how many different game-night configurations are possible now?

**Answer**: P(30, 7)

## Question 3 (3 points)

How many different 8-character passwords are possible if all uppercase (A-Z), lowercase (a-z), and digits (0-9) are allowed?

**Answer**: P(62, 8)

## Question 4 (3 points)

How many three-letter acronyms (arrangements of 3 alphabetic letters) are there with repetition allowed?  Assume uppercase (A-Z) only.

**Answer**: $(\frac{26}{3})$

## Question 5 (3 points)

How many three-letter acronyms (arrangements of 3 alphabetic letters) are there with repetition **not** allowed?  Assume uppercase (A-Z) only.

**Answer**: 15,600

## Question 6 (3 points)

How many different sequences can be formed using either two or three letters (A-Z) followed by either two or three digits (0-9)?

For example:
* AB01
* ABC12
* XY236
* XYZ123

**Answer**: P(37, 2) + P(37,3)

## Question 7 (4 points)

Suppose you flip a fair coin 10 times.  Determine how many ways you can get each of the scenarios in the table below.

|Scenario|Number of Ways|
|:-:|:-:|
|no heads|1|
|exactly one head|10|
|exactly two heads|45|
|at least two heads|1013|

## Question 8 (3 points)

Consider the following fruit that is available to you: raspberries, strawberries, blueberries, apples, oranges, bananas, kiwi, papaya, and mango.  Just choosing five from the list of 9, how many different combinations of fruit salad can you make?

**Answer**: 60,480

## Question 9 (3 points)

What is the number of different strings that can be formed by reordering the characters in the word `SUCCESS`?

**Answer**: $\frac{7!}{4!3!}$

## Question 10 (22 points)

### Part 1

Implement the `P` function and the `C` function to compute the $r$-permutation and $r$-combination, respectively for a set of size $n$.  You will need to use the `factorial` function provided in the `math` library in Python.

```python
from math import factorial
# factorial(6) = 6! = 720

def P(n,r):
    return factorial(n) // factorial(n - r)
    

def C(n,r):
    return P(n, r) // factorial(r)

```

### Part 2

Use the `P(n,r)` function you wrote to answer the following problems:

|Scenario|Answer|
|:-:|:-:|
|How many different arrangements can be made of 5 people from a group of 8 people to stand in line for a picture?|6720|
|How many different ways can 8 different projects be assigned to 26 people?  Only one project per person.  Not all people will be assigned to a project.|62990928000|
|How many different ways can we assign 15 pilots to 100 possible flight schedules?|331284225412682501619179520000|

### Part 3

Use the `C(n,r)` function you wrote to answer the following problems:

|Scenario|Answer|
|:-:|:-:|
|How many ways can we form a committee of 5 people from a group of 8 people?|56|
|How many ways can we select 8 people from a group of 26 people to work on a single project, assuming all people are equally qualified?|1562275|
|How many ways can we selet 15 winners for a vacation drawing from a group of 100 contestants assuming each prize is the same?|253338471349988640|


