# CSE 280 Prove 10

(c) BYU-Idaho - It is an honor code violation to post this
file completed or uncompleted in a public file sharing site.

**Instructions**: Answer each question using proper markdown notation as needed.  Use the preview view in Visual Studio Code (or another editor if desired) to see the formatting, tables, and mathematical formula properly rendered.  If you need to write code, then first test your code in a separate file and then copy the code into this document using code fences. 

**Name**: Geoffrey Collins

**Section**: 02

**Teacher**: Brother Macbeth

## Question 1 (5 points)

Evaluate the following as "True" or "False":

|Expression|Answer|
|:-:|:-:|
|$3 \vert 12$|True|
|$3 \vert 13$|False|
|$14 \vert 58$|False|
|$73 \vert 1752$|True|
|$73 \vert 1753$|False|

## Question 2 (5 points)

Given the following expressions, solve for $n$:

|Expressions|$n$|
|:-:|:-:|
|$n \text{ div } 11 = 4 \text{ , } n \text{ mod } 11 = 3$|47|
|$n \text{ div } 5 = 8 \text{ , } n \text{ mod } 5 = 1$|41|
|$n \text{ div } 7 = 9 \text{ , } n \text{ mod } 7 = 0$|63|
|$n \text{ div } 15 = 4 \text{ , } n \text{ mod } 15 = 7$|67|
|$n \text{ div } 13 = -2 \text{ , } n \text{ mod } 13 = 3$|-23|

## Question 3 (6 points)

For the given values of $x$, $y$, and $m$, determine if $x \equiv y (\text{mod } m)$ by marking "Yes" or "No" in the congruence column.

|$x$|$y$|$m$|$x \equiv y (\text{mod } m)$|
|:-:|:-:|:-:|:-:|
|24|32|3|No|
|24|80|7|Yes|
|83|59|8|Yes|
|222|122|10|Yes|
|17|6|5|No|
|81|37|11|Yes|

## Question 4 (15 points)
Find the GCD and LCM of the following numbers shown in non-decresasing prime factorization format.  Write your answers using non-decreasing prime factorization.  The first GCD one is done for you.

|$x$|$y$|$GCD(x,y)$|$LCM(x,y)$|
|:-:|:-:|:-:|:-:|
|$2^3 \sdot 3^2 \sdot 5$|$2 \sdot 3^3 \sdot 5^2 \sdot 7$|$2 \sdot 3^2 \sdot 5$|$2^3 \sdot 3^3 \sdot 5^2 \sdot 7$|
|$2 \sdot 5^3 \sdot 7 \sdot 11^2$|$2^3 \sdot 3 \sdot 5 \sdot 11$|$2 \sdot 5 \sdot 11 $|$2^3 \sdot 5^3 \sdot 7 \sdot 11^2$|
|$2^2 \sdot 3 \sdot 7^2 \sdot 13$|$2 \sdot 3^2 \sdot 5 \sdot 7 \sdot 13^2$|$2 \sdot 3 \sdot 7 \sdot 13$|$2^2 \sdot 3^2 \sdot 5 \sdot 7^2 \sdot 13^2$|

## Question 5 (7 points)

Find the numbers in the set $S$ that are part of the equivalance relation $\mathbf{R}_7$.  In other words, find the numbers that are congruent $(\text{mod } 7)$ and put them into the appropriate equivalance classes in the table below.

$S = \lbrace -48, -26, 1, 8, 3, 70, 24, 32, 11, 5, 27, 19, 49 \rbrace$

|Equivalence Class|Values in Equivalance Class|
|:-:|:-:|
|$[0]$|$\lbrace 70, 49 \rbrace$|
|$[1]$|$\lbrace -48, 1, 8 \rbrace$|
|$[2]$|$\lbrace -26 \rbrace$|
|$[3]$|$\lbrace 3, 24 \rbrace$|
|$[4]$|$\lbrace 32, 11 \rbrace$|
|$[5]$|$\lbrace 19, 5\rbrace$|
|$[6]$|$\lbrace 27 \rbrace$|

## Question 6 (12 points)

The python code below computes the GCD and LCM for two integers $x$ and $y$.  The GCD function is implemented for you.  Complete the LCM function.  Use the test code to verify your code.

```python
def gcd(x,y):
    for n in range(min(x,y),1,-1):
        if x % n == 0 and y % n == 0:
            return n
    return 1

def lcm(x, y):
    if x == 0 or y == 0:
        return 0
    else:
        return (x // gcd(x, y)) * y

print(gcd(12,15)) # 3
print(gcd(12,24)) # 12
print(gcd(12,18)) # 6 
print(gcd(7,13))  # 1
print(gcd(1,2))   # 1
print(gcd(5,5))   # 5
print("===================")
print(lcm(12,15)) # 60
print(lcm(12,24)) # 24
print(lcm(12,18)) # 36 
print(lcm(7,13))  # 91
print(lcm(1,2))   # 2
print(lcm(5,5))   # 5
```
