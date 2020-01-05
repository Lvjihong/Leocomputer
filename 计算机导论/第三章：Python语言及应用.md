第三章：Python语言及应用  
[TOC]  
# 计算机编程基本概念  
## 1. 程序（program）：  
为解决某一问题而设计的一系列指令，能被计算机识别和执行。  
## 2. 程序设计语言：  
用于书写计算机程序的语言。人与计算机打交道时交流信息的一类媒介和工具，由语句（statement）组成。  
## 3. 机器语言:（machine language）  
- 计算机直接使用的二进制形式的程序语言或机器代码。   
- 以二进制代码表示指令集合、CPU直接能识别和执行的语言。  
- 优点是占用内存少、执行速度快；缺点是不易阅读和记忆、编程查错困难等。  
## 4. 汇编语言：（assembler language）  
- 一种面向机器的用符号表示的低级程序设计语言。相当于机器指令的助记符号，与机器语言很接近。  
- 用助记符表示机器指令中操作码和操作地址的语言  
- 汇编语言也是面向机器的语言，与机器语言相比较为直观、易理解和记忆，但通用性不强。  
- 常用的汇编语言有80X86汇编、80C51汇编、ARM汇编等。  
## 5. 高级语言：（high－level language）  
- 是易为人们所理解的完全符号化的程序设计语言。  
- 接近人们使用的自然语言，一条语句不仅仅是完成单一的机器指令操作，也可能是多项操作。  
# 语言的层次  
![语言的层次](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\语言的层次.png)
![语言的层次2](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\语言的层次2.png)

## 编译系统  
由于计算机只能识别和执行机器语言，高级语言编写的程序仍然不能直接被计算机识别，必须经过 "翻译" 才能被执行。这种翻译方式有两种：编译、解释。负责这种翻译工作的程序称语言处理程序：编译程序、解释程序，它们均是系统程序。  
### 编译类语言  
编译类语言：编译是指在应用源程序执行之前，就将程序源代码 "翻译" 成目标代码(机器语言)，因此其目标程序可以脱离其语言环境独立执行，使用比较方便、效率较高。但应用程序一旦需要修改，必须先修改源代码，再重新编译生成新的目标文件才能执行，只有目标文件而没有源代码，修改很不方便。  
### 解释类语言  
解释类语言：执行方式类似于日常生活中的  "同声翻译" ，应用程序源代码一边由相应语言的解释器 "翻译" 成目标代码(机器语言)，一边执行，因此效率比较低，而且不能生成可独立执行的可执行文件，应用程序不能脱离其解释器，但这种方式比较灵活，可以动态地调整、修改应用程序。  
# 初窥高级语言  
## 高级语言的特点  
- 高度封装，与低级语言相对  
- 使用人易于接受的文字来表示  
- 不是特指的某一种语言，而是包括很多种  
- 与计算机的硬件和指令系统无关  
- 执行速度慢  
## 高级语言的语法  
不同的高级语言有不同的编写格式和语句分割符号，计算机按照语句分割符号识别每一条语句。语言的语法是指这样一组规则，用它可产生一个程序。
- 词法规则  
- 语法规则  
### 词法规则  
- 字母表就是一个有穷字符集  
∑ = { a—z 、 A—Z 、 0—9 、 (、 )、 [、 ]、 .、 !、 ~、 +、 -、 *、 /、 &、 %、 <、 >、 =、 ^、 |、 ?、 ,、 ; }  
- 词法规则是指单词符号的形成规则  
字母、下划线打头的字母、数字和下划线构成的符号串。如：a1、ave 、_day  
对语言来说，如何判定句子是否正确？规定句子是否正确的规则称为文法。为了能够正确理解句子，就需要先将句子拆分成多个单词。对自然语言这叫做分词；对编程语言，则叫做词法分析。   
### 语法规则（课本P8） 
- 语法规则规定了如何从单词符号形成更大的结构，换言之，语法规则是语法单位的形成规则。  
- 最常用的三种语句：  
1. 表达式语句  
2. 函数调用语句  
3. 控制语句  
### 高级语言的数据类型  
一个值的集合以及定义在这个值集上的一组操作，数据类型的出现是为了把数据分成所需内存大小不同的数据  
数据类型  
- 分得多大空间  
- 表示多大范围  
- 能做何种运算  
### 高级语言的表达式语句  
表达式语句由表达式组成。有算数表达式和布尔表达式  
表达式：操作数＋运算符  
表达式形成规则：  
- 表达式由数字、运算符、数字分组符号（括号）、变量等组成的有意义的序列，并且能够求得数值。  
- 执行表达式语句就是计算表达式的值。  
y+z是一个不完整表达式  
x=y+z是一个完整表达式  
### 函数调用语句  
函数调用语句由函数名和函数的实际参数所组成。
例如：
已有函数 add(y, z)，功能是两个参数求和函数调用语句： x=add(y, z) 。
### 控制结构  
- 顺序语句  
顺序结构是最简单的程序结构，也是最常用的程序结构，只要按照解决问题的顺序写出相应的语句就行，它的执行顺序是自上而下，依次执行。  
- 分支语句  
选择程序结构用于判断给定的条件，根据判断的结果判断某些条件，根据判断的结果来控制程序的流程。  
- 循环语句  
循环结构可以减少源程序重复书写的工作量，用来描述重复执行某段算法的问题，这是程序设计中最能发挥计算机特长的程序结构 。  
# 列举高级语言  
## 高级语言时代（1954—1995）   
随着世界上第一个高级语言FORTRAN的出现，新的编程语言开始不断涌现出来。各有特色，各有优势，随着时间的检验，一些流行至今，一些则逐渐消失。1957年世界上第一个高级语言FORTRAN 开发成功。 FORTRAN取的是FORmula TRANslator两个单词前几个字母拼成的，意思是公式翻译语言 。  
## 被遗忘的PASCAL  
- 1967年Niklaus Wirth开始开发PASCAL语言，1971年完成。  
- 主要特点有：严格的结构化形式；丰富完备的数据类型；运行效率高；查错能力强，可以被方便地用于描述各种算法与数据结构有益于培养良好的程序设计风格和习惯。   
- PASCAL是一个重要的里程碑结构化程序设计概念的语言。  
## C语言  
- 语言简洁紧凑、使用灵活方便。  
- 运算符丰富。  
- 数据类型丰富。  
- C是结构式语言。  
- 语法限制不太严格、程序设计自由度大。  
- 允许直接访问物理地址，可直接对硬件进行操作。  
- 程序执行效率高。  
- 适用范围大，可移植性好。  
## C++的特点  
- 保持了与C语言的兼容性。  
- 支持面向过程的程序设计。  
- 具有程序效率高、灵活性强的特点。  
- 具有通用性和可移植性。  
- 具有丰富的数据类型和运算符，并提供了强大的库函数。  
- 具有面向对象的特性，C++支持抽象性、封装性、继承性和多态性。  
## C#  
- C# 充分借鉴了 C 和 Java 的语言，甚至照搬了 C 的部分语法几乎集中了所有关于软件开发和软件工程研究的最新成果。面向对象、类型安全、组件技术、自动内存管理、跨平台异常处理、版本控制、代码安全管理 …  
- C# 程序需要 .NET 运行库作为基础 。  
## Java  
- Java语言是一个完全面向对象的语言，并且对软件工程技术有很强的支持。  
- Java语言的设计集中于对象及其接口，它提供了简单的类机制以及动态的接口模型。  
- 对象中封装了它的状态变量以及相应的方法，实现了模块化和信息隐藏。  
- 类提供了一类对象的原型，并且通过继承机制，子类可以使用父类所提供的方法，实现了代码的复用。  
# Python  
## Python简介  
### python的特点  
- 简单易学  
- 丰富的库  
- 可扩展、可嵌入  
- 面向对象、高层  
- 解释性  
- 免费开源、可移植  
### python的发展  
- 1991年，第一个Python编译器诞生  
- Python2.7将在2020年停止支持，并且不会在发布2.8版本  
## python的内置数据类型  
Python数据类型基本分为：数值类型、字符串类型、布尔类型  
Python组合数据类型包括：序列（列表、元组（不可更改的列表）、字符串）***有顺序编号的机构称为“序列”***、字典等
### 数值类  
#### 整数类型  
通常整数表示范围-2147483648~2147483647  
Python3.0后五范围限制  
操作符：+，-，*，%，（），/，//，**  

#### 浮点类型  
有小数部分的（包括5.0）***注意：10/5=2.0；10//5=2***  
操作符：+，-，*，（），/，//，**  

#### 随机数  
在Python中要产生随机数，首先要引入random模块。  
eg:产生10~20的随机浮点数  
```Python
import random  
f = random.unifort(10,20)
print(f)
```
eg:产生10~20的随机整数  
```Python
import random 
f = random.randint(10,20)
print(f)
```
### 布尔类型  
![布尔类型](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\布尔类型.png)
- 布尔型变量有两种可能的值：True  False  
- 布尔比较运算：<，>，<=，>=，==，!=   
- 布尔逻辑运算：not，and，or  
### 列表  
#### 列表的声明形式（列表中的元素以","相隔）  
1. L = []代表空列表  
2. L = [1，3，5]  
- 列表中的元素类型可以是不一样的，优点：给编程者带来许多便利；缺点：对列表元素操作时需要注意元素类型  
#### 序列的通用操作（包括列表、元组、字符串）  
1.索引  
- 序列中所有元素都有索引号  
- 索引号为正数时，从0开始递增  
- 索引号为负数时，表示从序列的最后一个元素开始计数   
eg：seq[2]:获得下标为2的元素  
2. 分片  
 L[index1:index2]（index1为分片结果中的第一个元素，index2永远取不到）  
 L[index1:]（冒号后边为空意味到头了）  
 L[:index2]（冒号前边为空意味着从最一开始取）  
 L[:]（意味着全部）  
 L[index1:index2:stride]（stride为步长，步长默认为1，可以大于1，可以取负数，但不能为0）***前面的数字决定着取值范围，步长决定着取值方向。***
举例
``` Python
L = [5,8,4,99,54,44,18]
print(L[2:1])
结果为[]
```
``` Python
L = [5,8,4,99,54,44,18]
print(L[2:1:-1])
结果为4
```
``` Python
L = [5,8,4,99,54,44,18]
print(L[-1:-2])
结果为[]
```
``` Python
L = [5,8,4,99,54,44,18]
print(L[-1:-2:-1])
结果为[18]
```
``` Python
L = [5,8,4,99,54,44,18]
print(L[-2:-1])
结果为[44]
```
3. 加  
加法表示连接操作，***注意：进行操作的两个序列必须是相同的数据类型（字符串、列表、元组等）才能进行加的运算。***
4. 乘  
序列的乘法表示将原来的序列重复多次。
5. in  
检查某个元素是否属于序列（not in表示判断元素是否不属于序列）  
#### 序列的通用函数  
1. len(seq):返回序列seq的元素个数  
2. min(seq):返回序列seq中“最小值”  
3. max(seq):返回序列seq中“最大值”  
4. sum(seq[index1:index2]):序列求和（字符串类型不适合）  
#### 列表专用方法\函数    
设s = [1，2]
|函数|作用|参数|结果|
|:-:|:-:|:-:|:-:|
|s.append(x)|将一个列表添加到列表s的末尾|“3”|[1,2,"3"]|
|s.clear()|删除列表s所有的元素|无|[]|
|s.copy()|返回与s内容一样的列表|无|[1,2]|
|s.count(x)|统计元素x在列表中出现的次数|2|1|
|s.extend(t)|将列表t添加到列表s的末尾|['3''4]|[1,2,'3','4']|
|s.insert(i, x)|将数据x插入到s的第i号位置|0, '3'|['3', 1, 2]|
|s.pop(i)|将列表s第i号元素弹出并返回其值|0 或 无|1 或 2|
|s.remove(x)|删除列表s中第一个值为x的元素|1|[2]|
|s.reverse()|反转s中的所有元素|无|[2, 1]|
### 字符串类型  
#### 字符串的表示方法  
- 单引号：例：'hello world!'  
- 双引号  例："hello world!"  
注意：  
- ' ' 或 " " 本身只是一种表示方式，不是字符串的一部分  
- 使用  ' '  表示字符串时，其中可以直接出现 "  
- 使用  " " 表示字符串时，其中可以直接出现 '  
- 字符串内既包含  ' 又包含  " 时，可在引号前边使用 \  进行转义  
- 字符串和字符不一样，字符常量占一个字节的内存空间，字符串常量占的内存字节数等于字符串中字节数加1。增加的一个字节用来存放字符‘\0’,作为字符串的结束标志。 
#### 字符串类型的部分应用  
- 字符串主要用在输入和输出，input( ) 函数为输入函数。
Python 的 input( ) 函数返回字符串类型
- 字符串类型与数值型相互转化  
1. 数值型转化成字符串类型  str( )  
2. 字符串类型转化成数值型  int( )（转化为整数） float( )（转化为浮点数）  
#### 字符串的格式化  
![字符串的格式化](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\字符串的格式化.png)  
- 常见转换说明符  
%s :  字符串     %d:整数  
%f :  浮点数     %r:不知道是啥  
%c：格式化字符及其ASCII码  
%o：格式化无符号八进制  
%x：格式化无符号十六进制数  
%X：格式化无符号十六进制数  
%f ：格式化浮点数字，可指定小数点后的精度  
%e：用科学计数法格式化浮点数  
%E：作用同%e，用科学计数法格式化浮点数  
%g：根据值的大小决定使用%f或%e  
%G：作用同%g，根据值的大小决定使用%f或者%E  
- 注意：  
不确定用什么时，%s  永远起作用，会把任何类型转换为字符串  
前边字符串里中有% 字符时，用 %%  转义来表示 % 。
#### 字符串转专用方法  
当 s = "Just do IT" 时  
|函数|作用|参数|结果|
|:-:|:-:|:-:|:-:|
|s.find(str,1,5)|字符串从1到4位置上中是否包含子字符串str，并返回位置索引|"do"|5|
|s.count(sub，1，5)|统计在1到4位置上sub出现的次数|"i"|1|
|s.strip(c)|移除字符串头尾指定字符|'T'|"Just do I"|
|s.lower()|将字符串的大写字母转小写字母|无|"just do it"|
|s.upper()|将字符串的小写字母转大写字母|无|"JUST DO IT"|
|s.swapcase()|将字符串大小写字母进行转换|无|"jUST DO it"|
|s.replace(old, new，count)|将字符串中的旧字符串替换为新字符串|"IT","it"|"Just  do it"|
|s.split(st)|将字符串根据分隔符st拆分成数列|" 有空格"|["Just", "do", "IT"]|
|s.capitalize()|首字母大写|无|"Just do it"|
|s.isalnum()|判断是否是字母或者数字(有空格也不行)|无|False|
|s.isalpha()|判断是否是字母|无|False|
|s.isdigit()|判断是否是数字|无|        False         |
```python
分离字符串
string = "www.gziscas.com.cn"
1.以'.'为分隔符
print(string.split('.'))
['www', 'gziscas', 'com', 'cn']
 
2.分割两次
print(string.split('.'，2))
['www', 'gziscas', 'com.cn']
 
3.分割两次，并取序列为1的项
print(string.split('.',2)[1])
gziscas
 
4.分割两次，并把分割后的三个部分保存到三个文件
u1, u2, u3 =string.split('.',2)
print(u1)—— www
print(u2)—— gziscas
print(u3) ——com.cn
```

### 字典  
![zidian](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\字典1.png)  
![zidian](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\字典2.png)  
## python赋值语句  
#### 基本赋值语句  
Python 中创建一个变量不需要声明其类型  
变量 = 值  
#### 序列赋值形式  
左侧的一系列变量 = 右侧的一系列值  
a,b,c = 1,2,3
#### 扩展序列赋值  
```Python
i,*j = range(3)
print(i,j)
结果为0，[1,2]
```
#### 多目标赋值  
```Python
i = j = k = 3
i = i + 2
print(i,j,k)
5 3 3
```
```Python
i = j = []
i.append(30)
print(i,j)
结果为[30][30]
```
```Python
i = [], j = []
i.append(30)
print(i,j)
结果为[30][]
```
#### 强调赋值  
i += 3等价于i = i + 3
```python
l = [1,2]
l1 = l
l += [4,5]
print(l,l1)
结果为[1,2,3,4][1,2,3,4]
```
```python
l = [1,2]
l1 = l
l = l + [4,5]
print(l,l1)
结果为[1,2,3,4][1,2,]
```
## python控制结构  
### if语句  
![if](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\if.png)  
```Python
def if_test(score): 
    if score >= 90: 
        print("Excellent") 
    elif score >= 80: 
        print("Very Good") 
    elif score >= 70: 
        print("Good") 
    elif score >= 60: 
        print("Pass") 
    else: 
        print("Fail") 
if_test(100)
```
### While语句  
- while
![while](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\while.png)  
- while-continue  
![while](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\while-continue.png)  
注意：遇到continue,结束本次循环，重新开始下一轮循环  
- while-break  
![while](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\while-break.png)  
注意：遇到break，结束整个循环，执行循环之后的语句  
- continue和break  
![while](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\continue和break.png)  
### for语句  
![for](D:\Github客户端\My Github\Leocomputer\计算机导论\图片\for.png)  
注意：object中的每一个元素会依次赋给target
## python函数调用  
函数定义：
def <函数名>(<形参列表>):
    <函数体>
函数调用：
<函数名>(<实参列表>)  
- 函数形参被赋值为实参  
1. 按位置对应，或按名（形参=实参），即位置和个数均一一对应  
2.  实参可以是字面值，也可以是已赋值的变量  
- 执行函数体
- 控制返回调用者（调用点的下一条语句）
#注意事项：  
1. "\n"表示换行，加在要换行的前边
```python
print("hello hello hello")
结果为:
hello hello hello
print("hello \nhello \nhello")
结果为:
hello
hello
hello
```
2. end=" "表示不换行，因为默认每打印一个结果都会换行  

# 1. 小练习  
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





