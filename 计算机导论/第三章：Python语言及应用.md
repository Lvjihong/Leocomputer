# 第三章：Python语言及应用  
## 1. 小练习  
```python
l = [4,5,1,2,0]
m = 0
for i in range(0,len(l)):
    if l[i]>l[m]:
     m = i
l[0],l[m] = l[m],l[0]
print(l)
```
```python
for i in range(1,10):
    for j in range(1,i+1):
        s = j * i
        print("%d * %d = %d" % (i,j,s),end=" ")
    print()
```
```python
import random
s = random.randint (2019012001,2019012100)
print("请学号为%d同学回答了老师问题！"%s)
```
```python
s = (input("请输入一个数："))
a = s[ : :-1]
if a==s:
    print("是回文数")
else:
    print("不是回文数")
```
一般排序：
```python
l = [4,5,1,2,0,10,6,11,15]
for j in range(0,len(l)-1):
    m = j
    for i in range(j,len(l)):
        if l[i]>l[m]:
          m = i
    l[j],l[m] = l[m],l[j]
print(l)
```
冒泡排序：
```python
l = [18,0,47,73,90,55,5,10]
for i in range(0,len(l)+1):
    for j in range(len(l)-1-i):
        if l[j]>l[j+1]:
            l[j],l[j+1] = l[j+1],l[j]
print(l)
```
快速排序：
```python
def F(data):
    if len(data) >= 2:  # 递归入口及出口
        mid = data[len(data)//2]  # 选取基准值，也可以选取第一个或最后一个元素
        left, right = [], []  # 定义基准值左右两侧的列表
        data.remove(mid)  # 从原始数组中移除基准值
        for num in data:
            if num >= mid:
                right.append(num)
            else:
                left.append(num)
        return F(left) + [mid] + F(right)
    else:
        return data
L = [1,5,9,6,5,66,8,2,3,3,4,7]
print (F(L))
```
```python
def f (x,y):
   print(x + y)
   return (x + y)
a = f(5,6)
print (a)
```
```python
def f (x,y,z):
    l = [x,y,z]
    for i in range (len(l)+1):
        for j in range(0,len(l)-i-1):
          if l[j]>=l[j+1]:
           l[j],l[j+1]=l[j+1],l[j]
    print("这三个数从小到大排列为",l)
f(5,8,1)

```
```python
def f():
    n = int(input("请"))
    while n != 0:
        print(n % 10)
        n = n // 10
f()
```
```python
global x
global y
global z
def f (x,y,z):
   if x > y:
       x,y = y,x
   if x > z:
       x,z = z,x
   if z > y:
       z,y = y,z
x = 2
y = 8
z = 1
f(x,y,z)
print("这三个数从小到大排列为%d,%d,%d"%(x,y,z))
```
```python
def f(n):
    s = 0
    for i in range (1,n+1):
        s = s + i
    return(s)
a = f(100)
print(a)

s = 1
for j in range(24):
    s = (s + 1) * 2
print(s)
```
```python
m = int(input("请输入一个大于0小于1000的正整数m："))
n = int(input("请输入一个大于0小于10的正整数n："))
s = m // n
a = m % n
if s < n:
    print(int(str(s) + str(a)))
else:
    t = str(a)
    while s != 0:
        b = s % n
        s = s // n
        t = str(b) + t
    print(int(t))
```
```python
m = int(input("请输入大于0小于1000的整数:"))
n = int(input("请输入大于0小于10的整数:"))
L = []
while m>0:
    a=m%n
    m=m//n
    L.append(a)
L.reverse()
for i in range(0,len(L)):
    print(L[i],end="")
```
```python
# # 游戏1.橙白诗韵
L =["李白","杜甫","辛弃疾","白居易","王安石","苏轼"]
S =["伤春悲秋","怀才不遇","爱国","送别","羁旅思乡"]
import random
i = random.randint(0,5)
j = random.randint(0,4)
x = L[i]
print("作者:%s"%x)
y =S[j]
print("风格:%s"%y)
print("请按上述要求说出两句诗。")
a = random.randint(1,9)
b = random.randint(1,7)
c = random.rannt("考虑专业知识方面，文院的要尽量贴合风格，软院的只要是这个作者就行。")dint(1,2)
if c==1:
   c="右"
else:
   c="左"
print("请%s侧的%d排的第%d的列同学起来颂诗"%(c,a,b))
```
```python
import random
a=random.randint(1,9)
b=random.randint(1,6)
i = random.randint(35,75)
j = random.randint(551,600)
print("请学号为20190146%d的文院小朋友上台参与"%i)
print("请学号为2019012%d的软院小朋友上台参与"%j)
```
```python
a = random.randint(1,9)
b = random.randint(1,7)
c=random.randint(1,2)
if c==1:
   c="右"
else:
   c="左"
print("请%s侧的%d排的第%d的列同学起来玩游戏"%(c,a,b))
可以成语接龙或者长篇诗词琵琶行之类的 一人一句
也可以表达对祖国的热爱 或列举国家70年的成就
```
```python
import jieba
from wordcloud import WordCloud
txt = "abcdefg"
words = jieba.lcut(txt)
newtxt =''.join(words)
wordcloud = WordCloud(font_path = " Iloveyou.ttf").generate(newtxt)
wordcloud.to_file('词云实例图.png')
```





