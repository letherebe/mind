```python
import turtle
def tree(branch, t):
    if branch < 5: return
    t.forward(branch)
    t.left(30)
    tree(branch*0.7, t)
    t.right(60)
    tree(branch*0.7, t)
    t.left(30)
    t.backward(branch)
t = turtle.Turtle(); t.speed(0); t.left(90)
tree(60, t)
turtle.done()
```
This Python code draws a fractal tree—each branch splitting endlessly, like thoughts branching from a single idea.