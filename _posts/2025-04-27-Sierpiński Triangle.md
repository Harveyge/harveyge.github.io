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

In 1915, Polish mathematician **Sierpiński** [Wikipeida](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_triangle) gave this shape its official math name, building on ideas from Georg Cantor’s work on “strange” sets that are everywhere yet take up zero space.
Nowadays folks discovered a playful way to “draw” it by randomly hopping halfway to triangle corners—no erasing needed! Dot. Dot. Dot. Suddenly, there it is.

You can also play the “Chaos Game”:
- Pick the three corners of a triangle on paper.
- Randomly choose a starting point anywhere inside.
- Repeat: randomly pick one of the three corners, then move halfway from your current point toward that corner, and put a dot.
- Keep doing this thousands of times.
  
simulate Sierpinski Triangle n=100
![simulate Sierpinski Triangle n=100](/assets/images/Sierpinski Triangle when n=100.png)
simulate Sierpinski Triangle n=1000
![simulate Sierpinski Triangle n=1000](/assets/images/Sierpinski Triangle when n=1000.png)
simulate Sierpinski Triangle n=10000
![simulate Sierpinski Triangle n=10000](/assets/images/Sierpinski Triangle when n=10000.png)

Now, let's play with the code. By changing the "n" variables in the code below, we can clearly see the evolution of the triangles.  
Play it in my [google colab](https://colab.research.google.com/drive/1nmMQXP5_PlsqR2GiE97NOby6FYsn4U_y#scrollTo=_b_xyx-hQ8JN) page.
