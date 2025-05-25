---
title: "Koch Snowflake"
layout: post
categories: blog
---

Imagine you start with a perfectly ordinary equilateral triangle

1. **The Little Triangle Trick**  
   - Take each side of your big triangle and chop it into three equal pieces.  
   - On the middle piece, stick out a smaller, pointy triangle—like giving your triangle a little hat.  
   - Boom! One straight side just turned into four zig-zag segments.

2. **Repeat Forever (or Until Bedtime)**  
   Do the same “chop-and-hat” dance on **every** straight segment you have, again and again. After a handful of rounds, that once-smooth triangle looks like a lacy, frosty snowflake—except it never truly finishes growing.

3. **Why It’s So Cool**  
   - **Endless Coastline Vibes:** The boundary keeps getting longer, like a coastline that never stops.  
   - **Finite Snowball:** Even though its edge stretches off toward infinity, the area inside tops out at a nice, finite size. 


![Koch Snowflake](/assets/images/Von_Koch_curve.gif)
[Source: Wikipedia](https://en.wikipedia.org/wiki/Koch_snowflake)

- **Fractal Antennas**  
In real world, I leared Koch Snowflake is useful for Antennas design.  Those jagged edges pack loads of “wire” into a small footprint—perfect for compact, multi-band antennas in phones, Wi-Fi routers, and satellites.


Swedish mathematician **Helge von Koch** published a short note to give a simple example of a curve that is continuous everywhere, but differentiable nowhere—challenging the then-prevailing intuition that most “nice” curves should have well-defined tangents at almost every point.

Now let’s play the draw a Koch Snowflake at different orders , using Python below:  
Notes: Because Google Colab cannot display Turtle window, need to use your local editor, for example Jupyter Notebook, to show the animation 



