<h1 align="center"> Etch-A-Sketch </h1>

```
from turtle import Turtle, Screen

etch = Turtle()
screen = Screen()
etch.speed(0)
screen.title("Etch-A-Sketch")
screen.bgcolor("light gray")


def move_forwards():
    etch.forward(10)
def move_backwards():
    etch.backward(10)
def clock_wise():
    etch.right(10)
def counter_clock_wise():
    etch.left(10)

def clear_drawing():
    etch.clear()
    etch.penup()
    etch.home()
    etch.pendown()


screen.listen()
screen.onkey(key="w", fun=move_forwards)
screen.onkey(key="s", fun=move_backwards)
screen.onkey(key="a", fun=counter_clock_wise)
screen.onkey(key="d", fun=clock_wise)
screen.onkey(key="c", fun=clear_drawing)


screen.mainloop()

```
