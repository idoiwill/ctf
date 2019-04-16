## 0x00 Exp
| 序号 | 类别       | 题目                                                         | 难度 | 要点                                                         |
| ---- | ---------- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| 1    | Misc：图像 | PlaidCTF 2019--Space Saver<br>[Writeup](https://github.com/Gdasl/CTFs/blob/master/PlaidCTF2019/SpaceSaver.md) | 低   | 1. PND的IEND后可以插入数据<br>2. flag图片在rar包中但加密了，解密的密码在另外图片里。隐藏在IEND后，将几张图片的IEND后字符拼接就是解密的密码 |
|      |            |                                                              |      |                                                              |
|      |            |                                                              |      |                                                              |

1. 当拿到shell，但限制了cat, more等命令时，不能显示flag，可尝试bash -v /home/flag
   解析：bash -v file，会打印file的内容并执行
