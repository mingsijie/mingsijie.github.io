title: Python程序设计例题（第四章）
url: 32.html
id: 32
categories:
  - Python初学
date: 2019-05-31 12:53:45
tags:
---
一、猜数字

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
<!--more-->
二、求水仙花数（第二版）

    for i in range(100,1000):
        si=str(i)
        n100 = int(si[0])
        n10 = int(si[1])
        n1 = int(si[2])
        if n100**3+n10**3+n1**3 == i :
            print(i)

三、判断回文

    n=input("input a number:")
    
    ##if n==n[::-1]:
    ##    print("yes")
    ##else:
    ##    print("no")
    
    print("yes" if n==n[::-1] else "no" )

四、生成回文

    s=input("input :")
    print(s+s[-2::-1])

五、凯撒密码

    #加密
    plaincode = input("请输入明文: ")
    for p in plaincode:
        if ord("a") <= ord(p) <= ord("z"):
            print(chr(ord("a") + (ord(p) - ord("a") + 3)%26),end='')
        else:
            print(p, end='')
    
    
    #解密
    plaincode = input("请输入明文: ")
    for p in plaincode:
        if ord("a") <= ord(p) <= ord("z"):
            print(chr(ord("a") + (ord(p) - ord("a") - 3)%26),end='')
        else:
            print(p, end='')