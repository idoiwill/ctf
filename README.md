# CTF套路
## 一、PWN
### 0x01 栈溢出
1.只允许输入可见字符的shellcode：<br>
XXj0TYX45Pk13VX40473At1At1qu1qv1qwHcyt14yH34yhj5XVX1FK1FSH3FOPTj0X40PP4u4NZ4jWSEW18EF0V<br>
https://www.exploit-db.com/exploits/35205/<br>

2.只允许输入少量类型的字符<br>
Blaze ctf 2018中的shellcodeme，shellcodeme这个ctf题目，利用7种类型的字符构造不同的指令，绕过输入的限制。<br>
参考writeup:<br>
https://github.com/ByteBandits/writeups/tree/master/blaze-ctf-2018/pwn/shellcodeme/sudhackar <br>
https://fortenf.org/e/ctfs/pwn/2018/04/23/blazectf-2018-shellcodeme.html<br>

3.需要Brute force canary（爆破栈cookie)<br>
参考：	http://www.pwntester.com/tag/exploit43/<br>

4.scanf<br>
scanf("%i",&a)，当输入是非数字的时候，不会写入到a。需要检查scanf的返回值。这种一般能利用绕过canary的检查，如pwnable.t的doublesort。<br>

### 0x02 堆溢出

### 参考
1. https://github.com/shellphish/how2heap

### 0x03 技巧
1. 题目用的是socket连接，直接调用system是无法返回shell的，可以用dup2，将0,1,2的文件描述符重定向到socket（4）<br>

## 二、Crypto
### 要点
1. 记住异或(^)，基础题的考点
2. 32个字符的，一般是MD5
3. 根据输入返回一个固定值，但是又不是其MD5，则有可能加了Salt，运算是xor，例子[MeePwnCTF2018-Ezchallz](https://blog.naver.com/mouse0333/221319793689)
### Tools
1. https://github.com/lovebed/rsatools
### 实用技巧
1. 十六进制字符串异或
```
>>> from pwn import *
>>> xor("b74c7f3802cff04ecdcf64bbe579fc73".decode('hex'),
"06e71f4c7b5be70f1687d55f9821d06e".decode('hex')).encode('hex') 
'b1ab607479941741db48b1e47d582c1d'
```
2. 各种转换
```
#16进制字符串转成整数
>>> int("b74c7f38",16)
3075243832L
#二进制字符串转成整数
>>> int("010111",2)
23
#
```
3. Padding

## 三、工具技巧
### 0x01 pwntools
1. 调用gdb
```
p = process('./xxxx')
if debug:
  gdb.attach(p, '''
set disassembly-flavor intel
set height 0
display/10i $pc
b *0x0000000000400712
display/ub ($rsp + 0x107)
''')
```
## 四、Other
### remove alarm
sed –i “s/alarm/isnan/g” yourbin
