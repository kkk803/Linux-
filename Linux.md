# Linux

ip addr 查看机器IP

systemctl status ssh 确保ssh服务器处于正常运行状态

exit 退出

## 基本指令

**pwd**

print working directory 打印当前工作目录

出现/，/叫做根目录，Linux的目录像一棵倒挂的树，最顶层的目录就是这个更目录

**ls**

list缩写，列表，把当前环境的文件像列表一样列一个清单

查看当前所在位置的目录，可能是文件或目录

在Linux中一切皆文件，更目录下这些都是目录，目录是特殊的文件

**cd**

cd:change directory 更改目录

***cd home*** 

每个账号对应一个自己的home目录，也称主目录，是账号的老家，进入home目录

进入home目录后，可以试试pwd ls，确定当前位置和周围环境

***cd ..***

从home目录退出到根目录

***ls /***

想查看根目录但是不改变自己在哪个目录

***cd /user/bin***

处于/home目录，想进入根目录下的user目录下的bin目录，这种写法叫做**绝对路径**

***cd ./../user/bin***

.表示当前，..表示上一级目录，这种写法叫做**相对路径**（./可以省略）

**clear**

清除屏幕

***ls -a***

查看更详细信息

***touch***

创建文件，touch file1 file2

***cat***

查看文件内容，cat file1

***rm***

删除命令，rm file1

***mkdir***

创建新目录，mkdir dir1

***cp***

复制文件到目录，cp+文件名+目录名

***mv***

将文件移动到目录，mv+文件名+目录名

在文件移动同时重命名文件，mv+文件名+目录名+/+文件名

***rmdir***

删除目录（空目录）

***rm -r***

rm -r dir1(删除非空目录)

***ls -l /***

l 对应long，长列表的格式展示信息，更加详细（4096是字节）

<img src="https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506081724395.png" alt="image-20250608172453304" style="zoom: 67%;" />

***ls -l -h /***

h对应human，以人类可读的方式来展示数据（将字节转换为人类可读的方式）

<img src="https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506081725920.png" alt="image-20250608172529869" style="zoom:67%;" />

**-h或者- -help**

**man手册**

man + 空格 + 命令查找学习对应的命令

![image-20250608173959874](https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506081739923.png)

![image-20250608174042790](https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506081740850.png)  

## Shell

 shell 本身 就是一个程序，跟别的程序并无不同。在linux系统下默认的shell 一般都是 bash。

**echo $SELL**

查看shell



linux命令有两种类型，程序名称和Sell内置命令

内置命令Shell直接执行

非内置命令Shell根据环境变量$PATH中设置的路径查找，即在指定位置查找对应的程序，找到对应的名字的程序后，shell会启动程序，并将参数传递给程序



**type**

判断内部命令还是程序

有的两个都不是，ll是“ls -lh”的别名

**data**

查看时间

### 快捷键

**ping  -c**

检测网络，c后加次数

**find /**

执行时间很长，结束进程用**Ctrl+C**，停止进程用**Ctrl+Z**



在ping的时候用**Ctrl+z**并没有结束，用**pidof ping**查看ping的进程号，用**ps+进程号**查看进程状态，发现进程仍然存在，只是状态成为了**T**，表示进程是被信号停止的，停止的进程可以输入**fg 1**重新运行起来，然后**Ctrl+C**如图是真正结束

![image-20250610111318198](https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506101113251.png)

![image-20250610111428910](https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506101114958.png)

**Tab**

补全快捷键，shell根据输入的内容结合系统环境尝试补充接下来想要输入的内容

![image-20250610124843192](https://cdn.jsdelivr.net/gh/kkk803/Picture-bed1@main/img/202506101248256.png)



**bash-completion**





bash编辑模式有两种，vi/emacs,分别对应软件vi/emacs的操作和快捷键

### **emacs模式下的快捷键**

**shopt -o emacs**

查看是否为emacs模式

**Ctrl + b/f**

移动光标的操作，分别表示向左和向右

**Alt + b/f**

以单词移动光标，分别表示向左和向右

**Ctrl + a/e**

移动光标到行首/行尾，和home/end一样

**Ctrl + d**

相当于delete，用于删除光标下的字符；还是Linux下的文件结束符

**openssl sha1 -hex**

执行一些大输入内容时，比如计算一段话的摘要值

