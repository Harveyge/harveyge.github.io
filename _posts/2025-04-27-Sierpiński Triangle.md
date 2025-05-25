---
title: "Sierpiński Triangle"
layout: post
categories: blog
---

Long before computers, artists in 16th-century lace-makers and stone-carvers loved repeating triangular holes in patterns.
Sierpinski triangle pattern in 11-13th'centries:[source](https://www.formulas.it/formulog/wp-content/uploads/2014/12/sierpinski-aplimat.pdf)

![Sierpinski triangle pattern in 11th centry](/assets/images/Sierpinski Triangle in stone 0.png)
![Sierpinski triangle pattern in 13th centry](/assets/images/Sierpinski Triangle in stone 1.png)

It is even more exciting that some seashell have similar pattern. 

![Sierpinski triangle pattern in seashell](/assets/images/Sierpinski triangle pattern in seashell.jpg)

An interesting video show the how to make it manually:
[![ Demonstrates The Sierpinski Triangle in Mathematical Visual](https://img.youtube.com/vi/Fgu5-3ihVVI/0.jpg)](https://www.youtube.com/watch?v=Fgu5-3ihVVI)


<div class="video-container">
  <iframe
    src="https://www.youtube.com/embed/Fgu5-3ihVVI"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>


In 1915, Polish mathematician **Sierpiński** [Wikipeida](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_triangle) gave this shape its official math name, building on ideas from Georg Cantor’s work on “strange” sets that are everywhere yet take up zero space.
Nowadays folks discovered a playful way to “draw” it by randomly hopping halfway to triangle corners—no erasing needed! Dot. Dot. Dot. Suddenly, there it is.

You can also play the “Chaos Game”:
- Pick the three corners of a triangle on paper.
- Randomly choose a starting point anywhere inside.
- Repeat: randomly pick one of the three corners, then move halfway from your current point toward that corner, and put a dot.
- Keep doing this thousands of times.
 

Play it in my [google colab](https://colab.research.google.com/drive/1nmMQXP5_PlsqR2GiE97NOby6FYsn4U_y#scrollTo=_b_xyx-hQ8JN) page.

- simulate Sierpinski Triangle n=100 
![simulate Sierpinski Triangle n=100](/assets/images/Sierpinski Triangle when n=100.png)

- simulate Sierpinski Triangle n=1000
![simulate Sierpinski Triangle n=1000](/assets/images/Sierpinski Triangle when n=1000.png)

- simulate Sierpinski Triangle n=10000
![simulate Sierpinski Triangle n=10000](/assets/images/Sierpinski Triangle when n=10000.png)


Leave your comments below!


<section id="comments">
  <script src="https://utteranc.es/client.js"
          repo="harveyge/harveyge.github.io"
          issue-term="pathname"
          theme="github-light"
          crossorigin="anonymous"
          async>
  </script>
</section>


## Python Code
```python
# Demo of piraling Through the Collatz Conjecture
# Description: Plot each term of a Collatz sequence in polar coordinates, and show the result
# of a swirling spiral
# Author: Daniel Ge
# Date:   2025-04-26

import random
import matplotlib.pyplot as plt

def sierpinski_triangle(n):

  A = (0,0); B = (1,0); C = (0.5, 0.866)
  x, y = 0.3, 0.4  # starting point
  points = []
    
  for _ in range(n):
      vertex = random.choice([A, B, C])
      x = (x + vertex[0]) / 2
      y = (y + vertex[1]) / 2
      points.append((x,y))

  xs, ys = zip(*points)
  plt.scatter(xs, ys, s=0.1)
  plt.axis('off')
  plt.show()

n = 100
#n = 1000
#n = 10000
sierpinski_triangle(n)
```
