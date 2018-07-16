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
4. 文件提取
```
openssl   rsautl -encrypt -in FLAG -inkey public.pem -pubin -out flag.enc
openssl   rsa -pubin -text -modulus -in warmup -in public.pem
```
