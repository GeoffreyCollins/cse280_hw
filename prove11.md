# CSE 280 Prove 11

(c) BYU-Idaho - It is an honor code violation to post this
file completed or uncompleted in a public file sharing site.

**Instructions**: Answer each question using proper markdown notation as needed.  Use the preview view in Visual Studio Code (or another editor if desired) to see the formatting, tables, and mathematical formula properly rendered.  If you need to write code, then first test your code in a separate file and then copy the code into this document using code fences. 

**Name**: Geoffrey Collins

**Section**: 02

**Teacher**: Brother Macbeth

## Question 1 (9 points)

Find the $gcd$ for each of the following by hand using Eulid's Algorithm  Show your work in the tables below.  The first one is done for you.  Add more rows to each table as needed.  You can check your work with a calculator.

**Problem A**: $gcd(43,57)$

|$x$|$y$|$r = y \mod x$|
|:-:|:-:|:-:|
|43|57|14|
|14|43|1|
|1|14|0|

Answer: 1

**Problem B**: $gcd(39,501)$

|$x$|$y$|$r = y \mod x$|
|:-:|:-:|:-:|
|39|501|33|
|33|39|6|
|6|33|3|
|3|6|0|

Answer: 3 

**Problem C**: $gcd(110,765)$

|$x$|$y$|$r = y \mod x$|
|:-:|:-:|:-:|
|110|765|105|
|105|110|5|
|5|105|0|

Answer: 5 

**Problem D**: $gcd(443,899)$

|$x$|$y$|$r = y \mod x$|
|:-:|:-:|:-:|
|443|899|13|
|13|443|1|
|1|13|0|

Answer: 1 

## Question 2 (10 points)

Find the $gcd$ for the first three problems from Question 1 using the Extended Eulcid Algorithm to express the answer as a linear combination.  The first one is done for you.

|Problem|$gcd = s*x + t*y$|
|:-:|:-:|
|$gcd(43,57)$|$1 = 4*43 - 3*57$|
|$gcd(39,501)$|$3 = -77*39 + 6*501$|
|$gcd(110,765)$|$5 = 7*110 - 1*765$|


## Question 3 (8 points)

Find the multiplicative inverse for $x \text{ mod } n$ in the table below.  These numbers are smaller so you don't need to use the Extended Euclidean Algorithm to solve.  You can check your answers by verifying that $sx \text{ mod } n = 1$ where $s$ is the multiplicative inverse you calculated.

|$x$|$n$|Multiplicative Inverse|
|:-:|:-:|:-:|
|2|7|4|
|5|11|9|
|7|20|1|
|3|13|9|

## Question 4 (9 points)
Use the Extended Euclidean Algorithm to find the multiplicative inverse of $83 \text{ mod } 96$.  You can check your answer by verifying that $s*83 \text{ mod } 96 = 1$ where $s$ is the multiplicative inverse you calculated.  

In your answer, provide both the linear combination of $1 = s*83 + t*96$ and the multiplicative inverse derived from it.

Answers:
* $s = -37$
* $t = 32$
* Multiplicative Inverse = 59

## Question 5 (14 points)

### Part 1

Create public and private RSA keys by selecting two prime numbers $p$ and $q$ that are in the range $[100,1000]$ (for performance reasons).  Don't select a $p$ and $q$ that we used in the reading or in classroom examples. Calculate $N$ and $\phi$.  Select a value of $e$ such that $gcd(e,\phi)=1$.  Find the multiplicative inverse for $e \text{ mod } \phi$ (called $d$).  You can use the following code to find the value of $d$.  This code implements the Extended Eculidean Algorithm and provides the GCD and the linear combination for the GCD.  If `x` and `y` are provided to the function, it will return a tuple `(r,s,t)` where `r` is the GCD and $r = s*x + t*y$.

```python
def gcd_ext(x,y):

    (old_r, r) = (x, y)
    (old_s, s) = (1, 0)
    (old_t, t) = (0, 1)
    while r != 0:
        q = old_r // r
        (old_r, r) = (r, old_r - q * r)
        (old_s, s) = (s, old_s - q * s)
        (old_t, t) = (t, old_t - q * t)
    return (old_r, old_s, old_t)
``````

Answers:
* $p = 419$
* $q = 797$
* $N = 333943$
* $\phi = 332728$
* $e = 65537$
* $d = 1$

### Part 2

The values of $N$ and $e$ are the public keys.  The value of $d$ is the private key.  Complete the python code below to encrypt the value $m = 5645$ and then decrypt it again. 

```python
# Put your values from Part 1
p = 419
q = 797
e = 65537
N = 333943
phi = 332728
d = 1

m = 5645

def encrypt(p, q, m):
    p = 419
    q = 797
    m = 5645
    e = 65537
    c = (m**e) % (N)
    return c

print(encrypt(p,q,m))

def decrypt(c, d, N):
    d = 1
    p = 419
    q = 797
    m_one = 5646
    e = 65337
    c = (m_one**e) % N
    m = c**d % N
    return m
    

print(decrypt(13906, 1, N))

```

  
