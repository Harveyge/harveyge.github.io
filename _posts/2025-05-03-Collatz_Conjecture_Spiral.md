---
title: "Visualize the Collatz sequence in Collatz spiral, that starts with any number"
layout: post
categories: blog
---

## What is the Collatz? 
    1. Pick any positive integer $n$
    2. If it’s even, divide it by 2($n$ -> $n$/2)
    3. If it’s odd, multiply by 3 and add 1 ($n$  -> 3 $n$+1)
    4. Repeat
    Once you hit 1, the “3×+1” rule sends you back into the loop 1→4→2→1 forever—like reaching the checkered flag in an infinite race.
    
## What is the Collatz map? 
A German mathematician named Lothar Collatz[Wikipeida] (https://en.wikipedia.org/wiki/Collatz_conjecture) posed a simple question:
    “What happens if we repeatedly apply this 3n+1 rule to any positive integer?”
Every number he tried eventually reached 1, and proposed this might be true for all numbers. Despite how easy it sounds, no one has ever proven it—it remains one of the biggest unsolved puzzles in math!
A "Collatz map" shows the correlation of any integer and it eventually envolved into 1! 

![Collatz map](/assets/images/collatz map.png)


Collatz spiral is a mordern visulization based on Collatz conjecture. 

![collatz_conjecture16](/assets/images/collatz_conjecture16.png)
![collatz_conjecture19](/assets/images/collatz_conjecture19.png)
![collatz_conjecture27](/assets/images/collatz_conjecture27.png)


Let’s play the spiral in Python!


Play it, by changing the "start" variables in the code below, or directly open my [google colab](https://colab.research.google.com/drive/13WyXPjfWPCNFrZ5iqiIkvVJ__Hy3Q3w1?usp=sharing) page.


## Python Code

```python
# Demo of piraling Through the Collatz Conjecture
# Description: Plot each term of a Collatz sequence in polar coordinates, and show the result
# of a swirling spiral
# Author: Daniel ge
# Date:   2025-05-03
import numpy as np
import matplotlib.pyplot as plt

def collatz(n):
    seq = []
    while n != 1:
        seq.append(n)
        n = n//2 if n%2==0 else 3*n+1
    seq.append(1)
    return np.array(seq)

start = 19
seq = collatz(start)
r = seq
theta = np.log(seq)

plt.figure(figsize=(6,6))
plt.plot(r*np.cos(theta), r*np.sin(theta), '-o', markersize=3)
plt.title(f"Collatz Spiral , start={str(start)})")
plt.axis('equal'); plt.axis('off')
plt.show()

start = 16
seq = collatz(start)
r = seq
theta = np.log(seq)

plt.figure(figsize=(6,6))
plt.plot(r*np.cos(theta), r*np.sin(theta), '-o', markersize=3)
plt.title(f"Collatz Spiral , start={str(start)})")
plt.axis('equal'); plt.axis('off')
plt.show()

```
