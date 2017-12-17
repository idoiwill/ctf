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
计算s的密文，得到:B9Hd7dhzY/4=<br>
计算evil的密文<br>

## Step 3
计算evil min<br>
1. min是可以直接算出来的，比如提交'jack min'，得到密文vgfZODJCSsvoIAOJX7VARQ==<br>
```python
[+] Downloading 'http://dictionary-attack.grandprix.whitehatvn.com:4321?plaintext=jack min&&ciphertext=': 1.88KB
Cipher text is  vgfZODJCSsvoIAOJX7VARQ==
```
其中4到8字节就是' min'的密文<br>
2. 再计算evil的值，可以用evils代替：<br>
```python
[+] Downloading 'http://dictionary-attack.grandprix.whitehatvn.com:4321?plaintext=evils&&ciphertext=': 1.87KB
Cipher text is  zvyKu3M8TaY=
```
其中0到4字节是'evil'的密文<br>
合并下即是'evil min'的密文<br>

## Step 4
计算'ds captu'的密文<br>
1. 计算'd'的密文<br>
2. 计算'is cap'的密文<br>
3. 计算'      t '的密文<br>
4. 计算'       u'的密文<br>
