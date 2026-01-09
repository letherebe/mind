```python
import turtle, random
turtle.speed(0)
for i in range(120):
    turtle.pencolor(random.random(),random.random(),random.random())
    turtle.forward(i*2)
    turtle.left(119)
turtle.done()
```
Draws a hypnotic spiral made of rainbow lines. Beauty in 7 lines.