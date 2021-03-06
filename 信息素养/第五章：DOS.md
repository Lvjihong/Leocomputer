[TOC]
# 常用DOS命令  
## DOS简介  
DOS — Disk Operating System  
现在已经是Windows时代，为什么还要提DOS？  
+ 计算机维护，有时需处理一些棘手问题  
+ 系统备份和恢复，也要进入纯DOS状态，并运行GHOST程序，涉及到DOS命令。  
## DOS基本知识  
### 盘符、光标、目录、路径  
#### 1.盘符  
盘符是DOS、WINDOWS系统对于磁盘存储设备的标识符  
在DOS命令里，盘符作如下表示：[单字母]:(即单字母+‘:’)  
例如：硬盘的第一个分区一般是C:(c:)；相应的，第二个分区是D:(d:)  
#### 2.光标  
所谓光标，就是DOS窗口中用来标志输入字符位置的一个符号(或标志，这也就是光标这个词的来源)  
键盘上控制光标按键  
![键盘上控制光标的按键](D:\Github客户端\My Github\Leocomputer\信息素养\图片\键盘上控制光标的按键.png)  
#### 3.目录  
目录就是桌面操作系统中的文件夹
通常我们将根目录定义为“\”，而一个目录与其子目录的分隔符，也用“\”分隔。
例如：\Student\Name，意思是从根目录起，第一级子目录为Student ，而Name是Student的子目录，也是根目录的第二级子目录；而Student\Name，意思则为， Student为当前目录的一个子目录，而Name则为当前目录的Student的子目录。  
无论是目录还是文件夹，在硬盘里，实际上都是一个树形结构，目录(文件夹)虽然可以放在目录(文件夹)里，但是，最外层的目录(文件夹)，实际上只有一个：在DOS下，最底层的目录，是根目录。而桌面系统里，最外层的文件夹，实际上就是各个分区。这样的树形结构，易于分类数据，便于硬盘上的数据和文件管理。  
#### 4.路径  
- 绝对路径  
- 相对路径  
### 文件名、文件通配符、文件属性  
#### 1.文件名  
在DOS中，文件名的长度限制为8个字符的文件名和3个字符的扩展名。 Windows桌面系统上的长文件名，在DOS状态下都变得面目全非。  
注：长文件名在纯DOS状态下的显示，是采用这样的方法：取长文件名的头六个字符加上一个“~”符号和一个一位的数字。  
![例如](D:\Github客户端\My Github\Leocomputer\信息素养\图片\例如.png)  
#### 2.文件通配符  
文件通配符是为了让DOS命令便于批量处理DOS文件，而采用的一种文件名的符号替换方法。
*是一个多字符的通配符，一个“*”可以搭配一个或多个字符。  
?是一个单字符的通配符，一个“?”只能搭配一个字符。  
#### 3.文件属性  
文件属性查看方式可以分为两种：  
- 第一种是指利用attrib命令  
- 第二种是指利用dir列表命令可以看到的文件特征  
1. 文档属性(A)：准备存档的文件。一旦创建，自带这个属性。这个属性一般不用理。  
2. 隐藏属性(H)：如果一个文件具有H属性，那么在dir时候，就看不到，只能利用加参数dir/ah,才能看到。  
3. 系统文件属性(S)：系统文件属性，是指这一个文件是系统文件，在系统启动和运行过程中可能会用到，不能被删除，也不能被编辑和修改。  
4. 只读属性(R)：如果一个文件具有R属性，则不能被编辑和修改。  
### 可执行文件  
可执行文件常见的有三类：EXE、COM和BAT  
- EXE和COM是可执行程序，它们所包含的是机器指令  
- BAT里面所记录的是一些可执行的DOS命令（DOS命令的集合），BAT能大大简化计算机维护人员的工作压力，你可以将你常用的一些DOS命令组合，做成把BAT文件。这样，就能有效的提高你的工作效率。  
## DOS命令  
### 切换盘符命令X: 
现在，我们引入一个当前盘的概念，当前盘，顾名思义，就是当前正在使用的盘(或分区)。如果要切换当前盘，就要使用切换盘符命令“X:”。  
例如：我们当前盘是C盘，如果想要切换到E盘，只需输入命令”E:”即可。  
### 改变当前目录cd(change directory)  
- 功能：改变当前目录	
- 类型：内部命令	
- 格式：cd  [盘符:][路径名]〈子目录名〉或  cd ..   或  cd \
c:\>cd fox\user（进入fox子目录下的user子目录）
c:\fox\user>cd .. (退回上一级根目录，注意cd后面跟着两个点"..“cd和点之间有空格)
c:\fox>cd \ （返回到根目录）
注：Cd 命令访问某个目录，可以进入到当前目录下的某个子目录中，只能一层一层走，不能越层，如需越层，则需要cd..或cd\   
### 建立子目录md(make directory)  
- 功能：创建新的子目录  
- 类型：内部命令  
- 格式：md [盘符:][路径名]〈子目录名〉  
### 删除子目录rd(remove directory)  
- 功能：从指定的磁盘删除了目录  
- 类型：内部命令  
- 格式：rd  [盘符:][路径名][子目录名]  
### 显示磁盘目录dir(directory)  
- 功能：显示磁盘目录的内容
- 类型：内部命令
- 格式：dir [盘符:][路径名][/p][/w][/A[[:]属性]][/O[:]排列顺序]][/S]*(注意：只有A和O后边有冒号，还是英文版的)*  
***说明：
（1）/p：分屏显示。当欲查看的目录太多，无法在一屏显示完屏幕会一直往上卷，加上/p参数后，屏幕上会分面一次显示部分行的文件信息，然后暂停，并提示；press any key to continue（按任意键继续）。
（2）/w：加上/w只显示文件名。至于文件大小及建立的日期和时间则都省略。加上参数后,每行可以显示五个文件名。
（3）/A： 显示具有指定属性的文件。
属性：D 目录      R 只读文件      H 隐藏文件      A 准备存档的文件     S 系统文件      
（4）/O ：用分类顺序列出文件。
排列顺序： N 按名称(字母顺序)      S 按大小(从小到大)          E 按扩展名(字母顺序)           D 按日期/时间(从先到后) 
（5）/S： 显示指定目录和所有子目录中的文件。***  
### 复制文件命令copy有两个作用  
1. 创建一个小型的文本文件：  
命令格式：copy con test.txt  
作用：将键盘上输入的文本信息以ASCII码的形式存储到test.txt文本文件中。  
注：在这里，DOS系统借鉴了UNIX系统的做法，将外部的输入和输出设备，作为文件来进行操作和处理。con代表的是标准输入，即键盘。
在输入完字符串以后，要以Ctrl+Z结尾，这样，才能完成整个命令。   
2. 复制文件  
命令格式1：copy 源盘或源目录  
命令格式2：copy 源盘或源目录 目的盘或目的目录  
- copy c:\*.*  
这个命令是将C盘根目录下的所有文件拷到当前目录下。  
- copy d:\txt\*.*  
这个命令是将D盘上，根目录下的txt子目录中的所有文件拷贝到当前目录下。  
- copy  c:\*.*  e:  
这个命令是将C盘根目录下的所有文件拷到E盘的当前目录下。  
- copy  a:\*.*  d:\txt   
这个命令是将软盘上的所有文件复制到D盘根目录下的txt子目录中。  
- copy  d:\txt\*.*  e:\txt   
这个命令是将D盘，根目录下的txt子目录中的所有文件拷贝到E盘的根目录的txt子目录中。  
- dir>testclass.txt  
- 这个命令是将应当输出到屏幕上的消息写入txt文本文档中。  
### 文件改名命令ren(rename)  
- 功能：更改文件名称  
- 类型：内部命令  
- 格式：ren [盘符:][路径]〈旧文件名〉〈新文件名〉  
### 删除命令del(delete)  
- 命令格式：del 目的文件
    例1：del  *.bak  
    这个命令是将当前目录下所有后缀名为.bak文件删除。  
    例2：del  c:\*.bak  
    这个命令是将C盘根目录下所有后缀名为.bak文件删除。  
    例3：del c:\*.*  
    这个命令是删除c盘所有内容的  
### 移动命令move  
- 命令格式1：move 源文件  
- 命令格式2：move 源文件 目的盘或目的目录  
- 功能：是将源文件移动到目的盘或当前盘下。
    ***move命令不推荐使用，因为可能存在安全问题。为什么？
    假设，你在移动大量文件时，如果在移动过程中意外停电，那么，你就可能有部分文件已经移动到目的盘，而还有部分文件保留在源盘上，这一结果很难处理。此外，还可能在停电时发生文件丢失的情况。所以，这个命令不推荐使用。***  
### 文件内容列表type  
- 命令格式：type 文本文件  
- 功能：是将指定文本文件的内容列出来。  
   例1：type test.txt  
   列出当前目录下，文本文件d.txt的内容。  
   例2：type c:\boot.ini   
   列出C盘根目录下，文本文件boot.ini的内容。  
### 文件属性命令attrib  
- 命令格式：attrib 命令参数 文件名  
attrib是一个功能强大的显示和修改文件属性的DOS命令。但是，要掌握它，也有一定的难度。前面，我们介绍过，文件有四个属性。分别是S(System),H(Hide),R(Read),A(Archive)。
- 用法：如果要给一个文件添加或去除某个属性，可以使用开关“+”和“-”。  
   例1：attrib -H +S *.txt  
   将当前目录下，后缀名为.txt的文件的隐藏属性去掉，并打开它们的系统文件属性。  
   例2：attrib -R -S -H *.sys  
   将当前目录下，后缀名为.sys的所有文件的R属性、S属性和H属性全部去掉。  
### 清屏 cls  
适用场合：屏幕上太乱了，或是屏幕上出现乱码了， 清除屏幕上显示内容但不影响电脑内部任何信息   
用法：cls　 回车  
### 显示及修改日期date  
- 适用场合：想知道或修改时间和日期   
- 用法：date 显示和改变当前日期  
例：C:\>date 08-20-2019  将日期改为2019年8月20日  
### 格式化 format　　  　
适用场合：执行快速格式化  
### ipconfig　　　  
适用场合：显示所有当前的 TCP/IP 网络配置值、刷新动态主机配置协议 (DHCP) 和域名系统 (DNS) 设置。使用不带参数的 ipconfig 可以显示所有适配器的 IP 地址、子网掩码、默认网关。  










