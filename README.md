# CTF套路
## PWN
### 0x01栈溢出
1.只允许输入可见字符的shellcode：<br>
XXj0TYX45Pk13VX40473At1At1qu1qv1qwHcyt14yH34yhj5XVX1FK1FSH3FOPTj0X40PP4u4NZ4jWSEW18EF0V<br>
https://www.exploit-db.com/exploits/35205/<br>

2.只允许输入少量类型的字符<br>
Blaze ctf 2018中的shellcodeme，shellcodeme这个ctf题目，利用7种类型的字符构造不同的指令，绕过输入的限制。<br>
参考writeup:<br>
https://github.com/ByteBandits/writeups/tree/master/blaze-ctf-2018/pwn/shellcodeme/sudhackar <br>
https://fortenf.org/e/ctfs/pwn/2018/04/23/blazectf-2018-shellcodeme.html<br>

### 0x02堆溢出
#### 参考
1. https://github.com/shellphish/how2heap

## Crypto
### Padding Oracle
### ECB
ECB的特点是同样的blcok，同样的密文
![](http://image.3001.net/images/20150115/14212875849501.png)
### Tools
1. https://github.com/lovebed/rsatools

## 工具技巧
### pwntools
1. 调用gdb
p = process('./xxxx')
if debug:
  gdb.attach(p, '''
set disassembly-flavor intel
set height 0
display/10i $pc
b *0x0000000000400712
display/ub ($rsp + 0x107)
''')

