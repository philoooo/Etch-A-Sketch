<h1 align="center"> Etch-A-Sketch </h1>

<div align="center">
<img src="https://github.com/philoooo/Etch-A-Sketch/blob/main/Screenshot%202025-10-30%20at%208.44.54%20PM.png" width="400" >
</div>

<h1></h1>

A fun little Python Turtle Etch-A-Sketch! Control the turtle with your keyboard (W/A/S/D) to draw on the canvas — press C to reset and start again.


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
