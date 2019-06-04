## 0x00 Exp
| 序号 | 类别             | 题目                                                         | 难度 | 要点                                                         |
| ---- | ---------------- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| 1    | 基础运算         | Plaid CTF 2019 - R u SAd?<br> [Writeup](http://duksctf.github.io/2019/04/13/PlaidCTF2019-rusad.html) | 低   | 1. 函数egcd(x,y)返回值a,b,c，表示等式a*x+b*y = c，利用该等式和已知变量进行替换变形，得到p/q；<br> 2.由于p和q都是素数，所以egcd的第三个返回值为1 |
| 2    | Java中random预测 | 强网杯，[Writeup](https://paper.tuisec.win/detail/d3216db087bae24) | 低   | Java的random函数实际是LCG，可以被预测。 参考Writeup里面的源码分析。 nextseed = (oldseed * multiplier + addend) & mask。这些都是已知的： ![image](https://cdn.tuisec.win/full/upload/201905/5dd823275963dd182a8220a04cdd7d19.jpg) |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |
|      |                  |                                                              |      |                                                              |



1. 当拿到shell，但限制了cat, more等命令时，不能显示flag，可尝试bash -v /home/flag
   解析：bash -v file，会打印file的内容并执行
