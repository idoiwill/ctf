# 思路
利用ECB的特点，算出每个单词的对应的密文，再拼接在一起<br>
dictionary的check是检查是否为英文单词或字母<br>
需要得到明文'evil minds captured flags'的密文<br>
因为blocksize = 8，所以将他分解为4个block<br>
evil min<br>
ds captu<br>
red flag<br>
s<br>
最容易的就是red flag和s这两个，因为都是单词，都不在黑名单里面。

## Step 1
计算red flag的密文，得到密文4IUNiM2KORvoIAOJX7VARQ==<br>
由于算法中有pad，所以前面8个字节才是密文<br>
```python
>>> '4IUNiM2KORvoIAOJX7VARQ=='.decode('base64')[:8]
'\xe0\x85\r\x88\xcd\x8a9\x1b'
>>> 
```
## Step 2
计算s的密文，得到：
计算evil的密文<br>
1. 先计算evils的密文为k0RmwH8kzkI=<br>
2. 前面4个字符的密文是
```python
>>> cp = 'k0RmwH8kzkI='
>>> cp.decode('base64')
'\x93Df\xc0\x7f$\xceB'
>>> 
```
