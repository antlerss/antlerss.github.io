---
title: 2020杭电CTF-WP
date: 2020-10-17 17:00:08
tags:
 - CTF
description: 活动
---


# 又见面了

看见后觉得是base64加密的

```
RlBJWkwlN0JTa2t6RXVhR21ncnQlN0QlMjBDbGFzc2ljYWwlMjBjcnlwdG8=
```

于是base64解码后得到，发现像URL编码

```
FPIZL%7BSkkzEuaGmgrt%7D%20Classical%20crypto
```

进行url解码

```
FPIZL{SkkzEuaGmgrt} Classical crypto
```

再进行凯撒解码，找到flag

```
ZJCTF{MeetYouAgaln} Wfummcwuf wlsjni
```



# 尺蠖求伸

得到文件后，IDA打开，查找字符串后找到flag

![2020杭电CTF (2)](https://antlers.oss-cn-hangzhou.aliyuncs.com/blog_images/CTF/2020%E6%9D%AD%E7%94%B5CTF%20%282%29.png)

进入后查看伪代码

![2020杭电CTF (1)](https://antlers.oss-cn-hangzhou.aliyuncs.com/blog_images/CTF/2020%E6%9D%AD%E7%94%B5CTF%20%281%29.png)

flag被base64加密了，于是进行解密，得到

```
ZJCTF{rE_15_H4rD_8U7_U5EfuL}
```

