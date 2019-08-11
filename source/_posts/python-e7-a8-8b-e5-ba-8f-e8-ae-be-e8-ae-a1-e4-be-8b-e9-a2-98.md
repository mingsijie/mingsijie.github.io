title: Python程序设计例题（第一、二章）
url: 24.html
id: 24
categories:
  - Python初学
date: 2019-05-31 12:41:22
tags:
---
第一章例题

    #计算圆周率
    from random import random,seed
    试验点数 = 10000000
    hits = 0.0
    seed(125)
    for i in range(1, 试验点数+1):
        x, y = random(), random()
        dist = pow(x ** 2 + y ** 2, 0.5)
        if dist <= 1.0:
            hits = hits + 1
    pi = 4 * (hits/试验点数)
    print("圆周率值是: {}".format(pi))
    print('与3.1415926相差：{}'.format(3.1415926-pi))
    
<!--more-->
第二章例题

    #货币汇率转换
    # def convert_currency(im, er):
    #     """
    #         汇率兑换函数
    #     """
    #     out = im * er
    #     return out
    
    
    def main():
        """
            主函数
        """
        # 汇率
        USD_VS_RMB = 6.77
    
        # 带单位的货币输入
        currency_str_value = input('请输入带单位的货币金额：')
    
        unit = currency_str_value[-3:]
    
        if unit == 'CNY':
            exchange_rate = 1 / USD_VS_RMB
    
        elif unit == 'USD':
            exchange_rate = USD_VS_RMB
    
        else:
            exchange_rate = -1
    
        if exchange_rate != -1:
            in_money = eval(currency_str_value[:-3])
            # 使用lambda定义函数
            convert_currency2 = lambda x: x * exchange_rate
    
            # # 调用函数
            # out_money = convert_currency(in_money, exchange_rate)
    
            # 调用lambda函数
            out_money = convert_currency2(in_money)
            print('转换后的金额：', out_money)
        else:
            print('不支持该种货币！')
    
    if __name__ == '__main__':
        main()
    

    #蟒蛇绘制
    import turtle
    
    snakeWidth = 25			# 蛇身体宽度
    snakeColor = 'purple'	# 蛇身体颜色
    snakeStepAngle = 40		# 蛇蜿蜒的角度
    snakeStepRadius = 40	# 蛇蜿蜒的半径
    snakeStepCount = 4		# 蛇蜿蜒的次数
    
    # 设置窗口和笔刷属性
    turtle.setup(650,350)
    turtle.pensize(snakeWidth)
    turtle.pencolor(snakeColor)
    
    # 把笔刷移动到左侧
    turtle.penup()
    turtle.fd(-300)
    turtle.pendown()
    
    # 绘制蜿蜒的部分
    turtle.setheading(-snakeStepAngle)
    for i in range(snakeStepCount):
    	turtle.circle(snakeStepRadius,snakeStepAngle*2)
    	turtle.circle(-snakeStepRadius,snakeStepAngle*2)
    
    # 让蜿蜒过后的身体朝向右侧水平位置
    turtle.circle(snakeStepRadius,snakeStepAngle)
    # 绘制一段水平的sentiment
    turtle.forward(snakeStepRadius)
    # 绘制扭头的部分
    turtle.circle(snakeStepRadius/2, 180)
    turtle.forward(snakeStepRadius)
    
    turtle.done()

    #绘制同切圆（1）
    import turtle
    turtle.pensize(5)
    turtle.pencolor("red")
    
    for r in (10,40,80,100):
        turtle.circle(r)
        turtle.goto(0,0)
        turtle.right(90)
        turtle.fd(r)
        turtle.left(90)
        

    #绘制同切圆（2）
    import turtle
    turtle.pensize(5)
    
    for (r,c) in ((10,"black"),(40,"red"),(80,"green"),(100,"blue")):
        turtle.pencolor(c)
        turtle.circle(r)
    

    #绘制同切圆（3）
    import turtle
    
    
    for (r,c,w) in ((10,"black",5),(40,"red",3),(80,"green",2),(100,"blue",4)):
        turtle.pencolor(c)
        turtle.pensize(w)
        turtle.circle(r)
        
    

    #同切圆变量赋值
    import turtle
    
    r=100
    c="black"
    w=5
    
    #(r,c,w) = (10,"black",5)
    #r,c,w = (10,"black",5)
    #r,c,w = 10,"black",5
    
    turtle.pencolor(c)
    turtle.pensize(w)
    turtle.circle(r)
        
    

    #同切圆
    import turtle
    turtle.pensize(5)
    
    turtle.circle(10)
    turtle.circle(40)
    turtle.circle(80)
    turtle.circle(160)
    
    

    #绘制同心圆
    import turtle
    ##turtle.setup(800,800,0,0)
    turtle.setup(1.,1.)
    turtle.screensize(800,800,"black")
    turtle.shape('turtle')
    turtle.pensize(5)
    turtle.pencolor('blue')
    turtle.circle(200)
    turtle.penup()
    turtle.goto(0,50)
    turtle.pendown()
    turtle.pencolor('red')
    turtle.circle(150)
    turtle.penup()
    turtle.goto(0,100)
    turtle.pendown()
    turtle.color('green')
    turtle.circle(100)
    
    
    turtle.exitonclick()
    
    

    #绘制太极阴阳
    import turtle
    import time
    r=50
    turtle.begin_fill()
    turtle.circle(r,180)
    turtle.circle(2*r,180)
    turtle.circle(r,-180)
    turtle.end_fill()
    
    turtle.seth(0)
    turtle.color("black","green")
    turtle.begin_fill()
    turtle.circle(r,180)
    turtle.circle(2*r,-180)
    turtle.circle(r,-180)
    turtle.end_fill()
    
    rEye = 15
    turtle.color("yellow","white")
    turtle.begin_fill()
    turtle.penup()
    turtle.goto(0,r+rEye)
    turtle.pendown()
    turtle.circle(rEye)
    
    turtle.penup()
    turtle.goto(0,-r+rEye)
    turtle.pendown()
    turtle.circle(rEye)
    turtle.end_fill()
    
    turtle.hideturtle()
    time.sleep(3)
    
    
    while  turtle.undobufferentries():
        turtle.undo()
    

    #绘制圆内接多边形
    import turtle
    r=100
    turtle.pensize(3)
    turtle.circle(r,steps=3)
    turtle.pencolor("red")
    turtle.circle(r,steps=4)
    turtle.pencolor("green")
    turtle.circle(r,steps=5)
    ##turtle.pencolor("blue")
    ##turtle.circle(r,steps=6)