## 0x00 Exp
| 序号 | 类别             | 题目                                                         | 难度 | 要点                                                         |
| ---- | ---------------- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| 1    | 基础运算         | Plaid CTF 2019 - R u SAd?<br> [Writeup](http://duksctf.github.io/2019/04/13/PlaidCTF2019-rusad.html) | 低   | 1. 函数egcd(x,y)返回值a,b,c，表示等式a*x+b*y = c，利用该等式和已知变量进行替换变形，得到p/q；<br> 2.由于p和q都是素数，所以egcd的第三个返回值为1 |
| 2    | Java中random预测 | 强网杯- randomstudy<br>[Writeup](https://paper.tuisec.win/detail/d3216db087bae24) | 低   | Java的random函数实际是LCG，可以被预测。 参考Writeup里面的源码分析。 nextseed = (oldseed * multiplier + addend) & mask。这些都是已知的，但是有个坑是移位后有强制转换。 |
| 3    | LLL attack       | 强网杯copperstudy<br>[Writeup](https://zhuanlan.zhihu.com/p/67180091) | 高   | CopperSmith相关知识：<br>1. 已知n,e,c和m的大部分比特位，且e=3<br>2. |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |


## 0x01 Other
1. 当拿到shell，但限制了cat, more等命令时，不能显示flag，可尝试bash -v /home/flag
   解析：bash -v file，会打印file的内容并执行
2. RSA攻击的很多原理，都总结在[这里](https://paper.seebug.org/727/)


## 0x02 ...

-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEAwm828+GZ1lFQipzX8IHl6MWpwPkrGFcwFpmqMthMDZh/fWsP8uQbLzgcX3P/
ITdW2OSpHO4gY+NnnJwiRS5MzAgWn+LZUHP1TsC5FqUbvBnKbBqyEMUIOwbNV2VwRqzGJ0H62RTB
VeV4kRxxqYtD6M1kp899zMj8Pvz4qzwbUh6bi8Mtxzr7VNhdHGmDyeCPTXG1QMDHCYXnHGY++++D
d5Ys/+tnpru/Rmn++ixEskPCXXrc0lLoc/3cDxuQlRPa/BOCNMpudM/PLs8A2gUFXDPmOt9VnUte
JD+JQTE3NOdCldAVnJ1WXabZo5GxPN7dGroNtXs1bc1k34WvgFYboQIDAQABAoIBABhat+ZqfsuC
mfUS2lWM39B9WdsLGuPMoABktRXzU+tsC6QZEgFZozIR9DPcort1ZBJ86dXu2e3JIURTplNGDmaM
KNFUJ+ZU8AgySbzVZ5jzHhDWczF4jKRgIL5uvVaM87EdKZ+hYuoweR6sEmyrPhFeENqYOei50CbP
pxJD0CRD6xqN0/9XolSu1DUdpgoGrRt4B7S2aBLQjb9udmChGksqMkHfFNB5SDyEuw/1Ug0zuoxZ
3nCOKwQriBWVFf1lOuceEhdjubbZ7Xn6BXINxP+5ZUBnVBLVp1FnT/ARIgosPXejNe6Oh/JhGN+v
5C7bYuXiNe63MWDuDKfFDDjoZoUCgYEA8437JfJo/o21wXvyrzyC9gB8zPllz6A+Pgm4LivnEtjD
3ocOF3nQbp6a6qIeEQLF0Nx5NOYly9SUy8D3VT7WzO4uoxPob1suFrfPwiISVnfg2p++wAtHU3xF
R45kpBQTg6Mf9uvCvP6iCvt5Rz3mfQu0wDvfSLqdPakqtA+Rws8CgYEAzF6tGbnzNb5WATLyKcqv
TNRr17I5SwMY7WZ/2uPyBSXGsUPWxinMM4DkBJLr3djpskH3ztQdCJdY9tLEaanG6m4KAbrRru+a
6XW77xmlD7TxD9p6ShjOndFXPZH1dI6fLcDNMrAXTRhCDBkuN3PVvGvLJddBLCh+aPTgJMMrlo8C
gYEA4lzwsqkl2oj9B9JakXINSfTUCXI2pQ2LK/++lfMp9gNPsJAXkcwe4+E3nKGGjkrkbiWr5XWO
ZW6zyNgVSL55x8gLwnfrTSwSnvzB9O3T21fZvXhBQp548WgLv+DhOvqJ1IwVVlpzCVMkak6lvogS
o9/wY8aB1UfUgw2qaeYalFMCgYBsMt/AVBNwa7HK9rcA6z7+FSR3UPNGRICJB5A/ShlTIlncdcca
qPxkdCPETCi2DmZDqutQxDoO11oRayrzqiAW82U23zquPEquuVdjUhdyhmBt/URrQFD7et6OSV1D
dVLO/VlmMZZUibhGAXrXfus003j9MsZdY57xYFve+rlz/wKBgB1vKlMscBx1xqWTtpnauSJGk/9c
Va7u2B7jA1KR6GkVMMgvNOM3rQyuaREZRyZOKirBqq4a2XiJbTYlsYqwWVMMspu7e6WeHXe6qDS3
oszf+u+YxgQ806AcHf7evjagHKFYQIwESCXJElxcMHJTeui6zXp6kFfwbVjyLxywKbg2
-----END RSA PRIVATE KEY-----
