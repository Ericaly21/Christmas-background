# Christmas-background
Christmas background for fun:)

import turtle
import random
# Uses at least two Turtles to draw the scene.
t = turtle.Turtle()
t2 = turtle.Turtle()
t3 = turtle.Turtle()
#Moon 
Moonturtle = turtle.Turtle()
#Snowman
Snowturtle = turtle.Turtle()

t.hideturtle()
t2.hideturtle()
t3.hideturtle()
Moonturtle.hideturtle()

#Get the screen and background color
def Draw_background():
  s = t.getscreen()
  s_width = 500
  s_height = 480
  s.setup(width = s_width, height = s_height)
  s.bgcolor("darkblue")


#Stars  
#Loop
#def draw_star(-80,190,'white',25)
#Draw first star
def Make_stars(l,x,y):
  t3.speed(50)
  t3.penup()
  t3.goto(x,y)
  t3.pendown()
  t3.hideturtle()
  t3.color('white')
#Uses for loop
  for i in range(5): 
#moving turtleforward 
    t3.forward(l) 
#rotating turtle 144 degree right 
    t3.right(144)


#Drawing Moon
def make_moon():
  Moonturtle.penup()
  Moonturtle.goto(-180,120)
  Moonturtle
  Moonturtle.hideturtle()
  Moonturtle.color('orange')
  Moonturtle.begin_fill()
  Moonturtle.circle(40)
  Moonturtle.end_fill()
  #Drawing moon crescent
  Moonturtle.up()
  Moonturtle.goto(-140,120)
  Moonturtle.color('dark blue')
  Moonturtle.begin_fill()
  Moonturtle.circle(50)
  Moonturtle.end_fill()


#Draw tree stem
def Draw_rectangle():
  t2.penup()
  t2.goto(-200,-92)
  align ='left'
  l = 20
  w = 30
  #Hideturtle
  t2.hideturtle()
  
  t2.begin_fill()
  t2.fillcolor("saddlebrown")
  t2.forward(l)
  t2.right(90)
  t2.forward(w)
  t2.right(90)
  t2.forward(l)
  t2.end_fill()

#Draw ornaments
def draw_ornaments(turtle, color, size, x, y):
  turtle.speed(30)
  turtle.hideturtle()
  turtle.penup()
  turtle.color(color)
  turtle.fillcolor(color)
  turtle.goto(x,y)
  turtle.pendown()
  turtle.begin_fill()
  turtle.circle(size)
  turtle.end_fill()
  
 #************* 
#Draw Snowman
def draw_snowman(color, radius, x, y):
  t.speed(150)
  t.penup()
  t.fillcolor(color)
  t.goto(x,y)
  t.pendown()
  t.begin_fill()
  t.circle(radius)
  t.end_fill()

 
def main():
  Draw_background()
  #Drawing the Snow
  t.penup()
  t.hideturtle()
  t.speed(50)
  t.fill(True)
  t.color("white")
  t.fill("white")
  t.goto(0,-100)
  t.setheading(180)
  t.forward(300)
  t.left(90)
  t.forward(140)
  t.left(90)
  t.forward(500)
  t.left(90)
  t.forward(140)
  t.left(90)
  t.forward(200)
  t.fill(False)
  t.penup()
  # Includes function to draw the main object (Stars..etc)
  #Draw multiple stars in various locations
  Make_stars(10,60,170)
  Make_stars(15,30,180)
  Make_stars(20,70,200)
  Make_stars(8,25,150)
  Make_stars(15,-10,200)
  Make_stars(5,-40,190)
  Make_stars(20,-80,200)
  Make_stars(7,-50,185)
  Make_stars(16,30,180)
  Make_stars(10,-70,160)
  Make_stars(6,-67,220)
  Make_stars(10,-90,215)
  Make_stars(13,90,160)
  Make_stars(15,100,218)
  Make_stars(8,85,220)
  Make_stars(10,45,215)
  Make_stars(5,30,200)
  Make_stars(8,-70,160)
  Make_stars(7,-35,150)
  Make_stars(10,-40,220)
  Make_stars(8,100,195)
  Make_stars(9,150,100)
  Make_stars(10,140,180)
  Make_stars(5,100,100)
  Make_stars(10,100,195)
  Make_stars(14,50,120)
  Make_stars(13,30,50)
  Make_stars(8,40,75)
  Make_stars(10,-25,65)
  Make_stars(15,-100,55)
  Make_stars(5,-50,50)
  Make_stars(12,-10,100)
  Make_stars(6,20,85)
  Make_stars(9,-100,120)
  Make_stars(8,-140,80)
  Make_stars(15,-180,90)
  Make_stars(15,-70,95)
  Make_stars(10,60,195)
  Make_stars(4,85,60)
  

  make_moon()
  #TREEstem
  Draw_rectangle()
  #Draw Christmas Tree
  #TreeTriangle Bottom
  side_length = 85
  angle = 120
  t.penup()
  t.left(angle)
  t.goto(-190,-30)
  
  t.pendown()
  angle = 120
  t.fillcolor('Darkgreen')
  t.begin_fill()
  t.forward(side_length) #drawbase
  
  t.right(angle)
  t.forward(side_length)
  
  #t.left(angle)
  #t.forward(side_length)
  t.end_fill()
  
  t.penup()
  
  #TreeTriangle Middle
  side_length = 60
  angle = 120
  t.penup()
  t.left(angle)
  t.goto(-190,-12)
  
  t.pendown()
  angle = 120
  t.fillcolor('Darkgreen')
  t.begin_fill()
  t.forward(side_length) #drawbase
  
  t.right(angle)
  t.forward(side_length)
  
  #t.left(angle)
  #t.forward(side_length)
  t.end_fill()
  
  t.penup()
  
  #TreeTriangle Top
  side_length = 30
  angle = 120
  t.penup()
  t.left(angle)
  t.goto(-190,-5)
  
  t.pendown()
  angle = 120
  t.fillcolor('Darkgreen')
  t.begin_fill()
  t.forward(side_length) #drawbase
  
  t.right(angle)
  t.forward(side_length)
  
  #t.left(angle)
  #t.forward(side_length)
  t.end_fill()
  t.penup()
  
  #Randomizing ornament colors
  #Uses a list
  ornament_list=["red", "purple", "blue", "yellow", "magenta"]
  for i in range(8):
    t.penup()
    x = random.randint(-210, -160)
    y = random.randint(-90, -40)
    size = random.randint(1, 3)
    colors = (random.choice(ornament_list))
    t.goto(x, y)
    t.pendown()
    draw_ornaments(t , colors, size, x, y)
    t.penup()
  
  #Below three statements for drawing snowman body
  draw_snowman("white", 15, 0, -3)
  draw_snowman("white", 25, 0, -25)
  draw_snowman("white", 40, 0, -55)
   
  draw_snowman("black", 2, -10, -10) #Draw left eye
  draw_snowman("black", 2, 10, -10) #Draw right eye
  draw_snowman("orange", 3, 0, -15) #Draw nose
   
  #draw snowman buttons
  draw_snowman("black", 2, 0, -40)
  draw_snowman("black", 2, 0, -50)
  draw_snowman("black", 2, 0, -60)
  
  #draw left arm
  t.penup()
  t.goto(-15,-50)
  t.pendown()
  t.pensize(3)
  t.goto(-40, -35)
  #draw right arm
  t.penup()
  t.goto(15,-50)
  t.pendown()
  t.pensize(3)
  t.goto(40, -35)
  
  #Draw hat
  t.penup()
  t.goto(-15, -5)
  t.color("black")
  t.pensize(5)
  t.hideturtle()
  t.pendown()
  t.goto(15, -5)
  t.penup()
  
  t.goto(-5, 20)
  t.fillcolor("black")
  t.begin_fill()
  t.pendown()
  t.left(90)
  t.forward(20)
  t.left(90)
  t.forward(12)
  t.left(90)
  t.forward(20)
  t.end_fill()
