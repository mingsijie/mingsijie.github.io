title: Python程序设计例题（第三章）
url: 29.html
id: 29
categories:
  - Python初学
date: 2019-05-31 12:49:33
tags:
---
1、给一个数，求其绝对值

    
    x=-123
    #xAbs=x if x>=0 else -x
    
    ##if x>=0:
    ##    xAbs=-x
    ##else:
    ##    xAbs=x
    
    xAbs=x
    if x<0:
        xAbs=-x
    
    print(xAbs)
    
<!--more-->
2、判断一个数的奇偶

    # 判别奇偶数
    x=1001
    
    if x % 2:
        print(x,"是奇数")
    else:
        print(x,"是偶数")
    
    #print(x,"是奇数") if x % 2 else print(x,"是偶数")

3、判别某年是否闰年

    """
    判断year是否为闰年
    """
    year =2001
    
    ##leap=False
    ##if year % 400 ==0 or year % 4==0 and year % 100!=0 :
    ##    leap=True
    leap=year % 400 ==0 or year % 4==0 and year % 100!=0
    
    if leap: print(year,"年是闰年")
    else:    print(year,"年不是闰年")

4、将分数成绩转为等级成绩

    
    score=44
    
    if score <60:
        grade = "不及格"
    elif score <70:
        grade = "及格"
    elif score <80:
        grade = "中"
    elif score <90:
        grade = "良"
    else:
        grade = "优"
    
    print(grade)
    

5、求“水仙花”数

    '''
    求水仙花数
    
    '''
    for i in range(100,1000):
        n100 = i//100
        n1 = i%10
        n10 = i%100//10
        if n100**3+n10**3+n1**3 == i :
            print(i)
    

6、猜数字

    right = 75#待猜数字
    not_found = True
    
    while not_found:
        guess=int(input("请猜数："))
        if guess==75:
            print("恭喜你猜对了！")
            not_found = False
        elif guess>75:
            print("猜大了")
        else:
            print("猜小了")