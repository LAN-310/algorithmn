在Python语言中最常见的括号有三种，分别是：小括号（）、中括号[]、花括号{}；其作用也不相同，分别用来代表不同的Python基本内置数据类型。

Python中的小括号（）：

代表tuple元祖数据类型，元祖是一种不可变序列。创建方法很简单，大多数时候都是小括号括起来的

1 >>> tup = (1,2,3)

2 >>> tup

3 (1, 2, 3)

4 >>> () #空元祖

5 ()

6 >>> 55,#一个值的元祖

7 (55,)
 

Python中的中括号[]：

代表list列表数据类型，列表是一种可变序列。创建方法既简单又特别。
 
原来list（）是调用函数啊，这样我就好理解的，那意思就是list('ABC')，调用了list这个函数，ABC就形成了一个有3个元素的列表，其中三个元素分别是A、B、C，而X=['ABC']，是本身列了一个列表，里面只有一个元素，元素是ABC

1 >>> list('Python')

2 ['P', 'y', 't', 'h', 'o', 'n']

那如果我要用调用list函数表示一个列表，里面只有一个元素，元素是ABC，怎么表示呢

 list(['ABC'])


Python中的花括号{}：

代表dict字典数据类型，字典是Python中唯一内建的映射类型。字典中的值没有特殊的顺序，但都是存储在一个特定的键（key）下。键可以是数字、字符串甚至是元祖。

1 >>> dic = {'jon':'boy','lili"':'girl'}

2 >>> dic

3 {'jon': 'boy', 'lili"': 'girl'}

dict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
 
dict['Age'] = 8 # 更新

dict['School'] = "RUNOOB" # 添加

python 类的定义与使用
---

为了代码的编写方便简洁，引入了类的定义；

一般，使用 class 语句来创建一个新类，class之后为类的名称(通常首字母大写)并以冒号结尾，例如:
```python
class Ticket():
    def __init__(self,checi,fstation,tstation,fdate,ftime,ttime):
        self.checi=checi
        self.fstation=fstation
        self.tstation=tstation
        self.fdate=fdate
        self.ftime=ftime
        self.ttime=ttime
    def printinfo(self):
        print("车次：",self.checi)
        print("出发站：", self.fstation)
        print("到达站：", self.tstation)
        print("出发时间：", self.fdate)
```

#类中可以定义所使用的方法，类的方法与普通的函数只有一个特别的区别——它们必须有一个额外的第一个参数名称, 按照惯例它的名称是 self；

#init()方法是一种特殊的方法，被称为类的初始化方法，当创建这个类的实例时就会调用该方法；

#self 代表类的实例，self 在定义类的方法时是必须有的，虽然在调用时不必传入相应的参数；

接下来是类的对象的创建：

```python
#创建a1对象
a1=Ticket("G11","xian","beijing",'2019-01-20','13:00','18:00')
#创建a2对象
a2=Ticket("T11","xian","beijing",'2019-01-21','13:00','19:00')
```

对象属性的访问：
```python
a1.printinfo()
a2.printinfo()
```
再举个例子：

```python
class Calculator:
    name="jisuanqi" #这是固有属性
    price=28
    #初始化，里面的参数可以自己定义
    def __init__(self,name,price,hight,width,weight):
        self.name=name
        self.price=price
        self.h=hight
        self.w=width
        self.weight=weight

    def add(self,x,y):
        print(self.name)
        result=x+y
        print(result)
    def subtract(self,x,y):
        print(x-y)
    def multiply(self,x,y):
        print(x*y)
    def divide(self,x,y):
        print(x/y)
#这里必须传入参数才可以
calc=Calculator('good calc',280,30,30,100)
print(calc.name)#jisuanqi
print(calc.weight)#100
print(calc.price)#280
```

" / "就表示 浮点数除法，返回浮点结果;" // "表示整数除法。
