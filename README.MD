# Linear Sieve Algorithm for Finding Prime Numbers & it's Performance Analysis

#### Design & Analysis of Algorithms (CS1501)

## Problem Statement

This repo has an analysis of some of the most popular prime
number evaluating algorithms until a given integer N.

The algorithms that have been tested are:

- Prime Number by trial division
- Optimized Prime
- Sieve of Eratosthenes
- Sieve of Atkin Algorithm
- Linear Sieve Algorithm

## Programs in Brief

### Prime Number by trial division
This is the most basic prime number evaluation algorithm, which does nothing but divides with every number until the limit and if
it finds the number is completely divisible it declares it as
composite otherwise as Prime.
######  Complexity: <img src="https://latex.codecogs.com/gif.latex?O(N^2)" title="O(N^2)" />

### Optimised Prime

This runs on the same concept of trial division but just benefits itself by the fact that it needs to only divide until Root(of Number) to check it’s primality.
###### Complexity: <img src="https://latex.codecogs.com/gif.latex?O(N&space;*\sqrt{N})" title="O(N *\sqrt{N})" />

### Sieve of Eratosthenes

This algorithms is one of the most popular prime number
finding algorithm. The idea is simple, initially it assumes all the
numbers are prime until the given limit and then it starts to
cross out the multiples of each number, Let say we needed to
find prime number until 100. Then Sieve of Eratosthenes would
assume initially assume all the numbers until 100 as prime and
then would start from 2, and mark it’s multiples as non prime
and similarly this would be done until it marks all the numbers
multiple of Root(100) as non prime. At last it simply displays the
resulting list of prime numbers

###### Complexity: <img src="https://latex.codecogs.com/gif.latex?O(N*\log\log&space;N)" title="O(N*\log\log N)" />

### Sieve of Atkin Algorithm

Note how in Sieve of Eratosthenes we're wasting time looking at all those even numbers even though we know that after 2 there aren't
any. So let's not mark them and hence not store them. We can also try this for 3. This would then be a mod-6 wheel since it will repeat after every 2*3=6 numbers.For 2/3/5 this can also be called a mod-30 wheel.The Sieve of Atkin Algorithm uses a mod-wheel and will skip multiples of 2, 3, and 5 just like  mod-30 wheel of Sieve of Eratosthenes.
We could divide the the values
that aren't multiples of 2, 3, or 5 in the mod-60 range into 3
groups, each with its own algorithm and each algorithm will give entries in the range that meet a quadratic equation like: 4x^2 + y^2 = 60k + delta, which then lets us do the normal
composite marking skipping forward by q^2.

###### Complexity: <img src="https://latex.codecogs.com/gif.latex?O(N/&space;\log\log&space;N)" title="O(N/ \log\log N)" />

### Linear Sieve Algorithm
The concept of linear Sieve is rather simple when compared with other Sieve of Atkin, when we were implementing Sieve of Eratosthenes, we were marking the multiples as non prime of a
specific number but this could be contradicting as for example, 6 is the multiple of rather 2 and 3 both, hence there is no point
in marking it again. This is what give Linear Sieve Algorithm advantage, but care must be taken while implementing it’s
algorithm as the function to get a number higher than N (in code) must be implement with least complexity possible.

###### Complexity: <img src="https://latex.codecogs.com/gif.latex?O(N)" title="O(N)" />

## Test Results

The test was carried to find out prime numbers until 10000 in the
sets of 5 to even out the error produced by the system it’s running
on. This gives all of the 5 algorithms 200 data points to plot it’s
graph and makes the complexity more visually apparent.

Bellow are the graph of input size vs time in seconds of each of the
5 algorithms.
![](https://abhinavutkarsh728.s3.amazonaws.com/Screenshot+2020-04-24+at+10.48.15+PM.png)
![](https://abhinavutkarsh728.s3.amazonaws.com/Screenshot+2020-04-24+at+10.48.24+PM.png)
![](https://abhinavutkarsh728.s3.amazonaws.com/Screenshot+2020-04-24+at+10.48.40+PM.png)

### Tested on:

- [Macbook Pro 2017 13“ Base Model](https://www.techradar.com/in/reviews/macbook-pro-with-touch-bar-13-inch-mid-2017)
- CPU clock 2.3 GHz
- RAM: 8GB (2,133MHz LPDDR3)
- Python Via Jupyter Notebook
- Time calculated via time library

#### Future Improvement:
As seen in few of the plots, we have sudden jump or downfall of time in between of an input size.
This could be because of kernel getting interrupted via some system process and hence giving us an anomalous behavior. These errors are supposed to be reduced in the future
implementations of these algorithms when measuring its complexity. In some cases we also noticed our linear algorithm taking more time to run which could be an issue with the writing of the code and hence it needs to be more optimized too.

## Conclusion

This report clearly shows how much of a difference Sieve of Atkin
has when compared with other Prime number evaluation algorithms
and hence the prefect balance between time and space complexity.
It further shows how much difference it can make by picking up the
right algorithm of prime number evaluation can have in areas of
Encryption for the calculation of private key by it’s public key.

###### References & Reading Material
- https://codeforces.com/blog/entry/
- https://www.cs.utexas.edu/users/misra/scannedPdf.dir/linearSieve.pdf
- https://www.hackerrank.com/topics/sieve-of-eratosthenes-linear-time
- https://www.quora.com/How-can-sieve-of-Atkin-be-explained-in-simple-terms
- https://www.geeksforgeeks.org/sieve-of-atkin/
- https://stackoverflow.com/questions/1023768/sieve-of-atkin-explanation
- https://brilliant.org/wiki/sieve-of-eratosthenes/
- https://www.geeksforgeeks.org/python-program-to-print-all-prime-numbers-in-an-interval/
- https://www.programiz.com/python-programming/examples/prime-number-intervals
- https://www.geeksforgeeks.org/analysis-different-methods-find-prime-number-python/
- https://www.geeksforgeeks.org/sieve-of-eratosthenes/
- https://www.khanacademy.org/computing/computer-science/cryptography/comp-number-theory/v/sieve-of-eratosthenes-prime-adventure-part-
- https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes
- https://cp-algorithms.com/algebra/prime-sieve-linear.html
- https://www.geeksforgeeks.org/sieve-eratosthenes-0n-time-complexity/



#### Installation

1. Install [Python](https://www.python.org)
2. Install [Jupyter Notebooks](https://jupyter.org)
3. In terminal run the command: $ jupyter notebook
4. CD to the code directory and run it
- Alternatively you can also make a .py by converting the .ipynb and then running it in an [IDE](https://www.jetbrains.com/pycharm/)