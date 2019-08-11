title: Python 语言程序设计基础第二章习题参考答案
url: 17.html
id: 17
categories:
  - Python初学
date: 2019-05-26 11:12:42
tags:
---
#书本P55页习题
<!--more-->
    import turtle
    import time
    #绘制直线
    turtle.fd(100)
    time.sleep(5)
    #清除屏幕并回到初始点
    turtle.clear()
    turtle.penup()
    turtle.setx(0)
    turtle.sety(0)
    turtle.pd()
    #让海龟飞起来！
    turtle.speed(30)
    #移动半径大小位置，并作圆
    inital_position = -20
    radium = 20
    for i in range(9):
        turtle.penup()
        turtle.sety(inital_position)
        inital_position = inital_position - 20
        turtle.pd()
        turtle.circle(radium)
        radium =radium + 20
    turtle.penup()
    turtle.setx(0)
    turtle.sety(0)
    turtle.pd()

    #书本P56页习题2.3
    import turtle as t
    t.setup(650,350,200,200)
    t.penup()
    t.setx(-250)
    t.pendown()
    t.pensize(25)
    t.seth(-40)
    color=["blue","red","yellow","green"]
    r=0
    for i in range(4):
        t.circle(40,80)
        t.circle(-40,80)
        t.pencolor(color[r])
        r = r + 1
    
    t.circle(40,80/2)
    t.fd(40)
    t.circle(16,180)
    t.fd(40*2/3)

    #书本P56页习题2.4+2.5
    from turtle import *
    import math
    penup()
    sety(100/3**(1/3))
    a=180+60
    pd()
    for i in range(3):
        seth(a)
        a=a+120
        fd(100)
    seth(a)
    fd(50)
    a = 0
    for i in range(3):
        seth(a)
        a=a-120
        fd(50)

    #书本P56页习题2.6
    from turtle import *
    import math
    penup()
    sety(100)
    setx(-100)
    a = -90
    for i in range(4):
        seth(a)
        fd(30)
        pd()
        fd(140)
        pu()
        fd(30)
        a = a +90

    #书本P56页习题2.7
    from turtle import *
    speed(1)
    for i in (270,210,150,90,30,-30):
        seth(i)
        fd(60)
        seth(i-120)
        fd(60)
        seth(i-240)
        fd(120)

    #书本P56页习题2.8
    from turtle import *
    speed(20)
    a = 1
    b = 0
    for i in range(1000):
        seth(b)
        fd(a)
        a = a+1
        b = b +90
    
    

[第二章作业](http://www.yeguang.me/wp-content/uploads/2019/05/第二章作业.zip)[下载](http://www.yeguang.me/wp-content/uploads/2019/05/第二章作业.zip)