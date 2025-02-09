---
title: blog test
tags: test
categories: 
excerpt: 这是文章摘要 This is the excerpt of the post
abbrlink: 432d8582
date: 2023-04-27 21:26:22
---

### 测试测试测试测试测试测试测试测试测试测试测试测试

[Theme Redefine Docs - Redefine Docs (ohevan.com)](https://redefine-docs.ohevan.com/)

## test img:

![坤坤](https://gitee.com/seahipage/my_pics/raw/master/from_windows/kunkun.png)



## test latex:

$$
test \ latex: y = x^2 + a
$$
Here is a Euler's formula:

$$
e^{i\pi}+1=0
$$
## test code:

```python
import cv2

# 打开默认摄像头
cap = cv2.VideoCapture(0) 

# 检查是否打开成功
if not cap.isOpened(): 
    print("Cannot open camera")
    exit()

while True:
    # 读取一帧
    ret, frame = cap.read()

    # 如果读取成功
    if ret == True: 

        # 显示图片
        cv2.imshow('frame',frame)

        # 判断用户是否按下q键
        if cv2.waitKey(1) & 0xFF == ord('q'):
            break

    # 如果读取失败
    else: 
        print("Can't receive frame (stream end?). Exiting ...")
        break  

# 释放摄像头并销毁所有窗口    
cap.release()
cv2.destroyAllWindows()
```

## Test note block

### 大提示块

{% notel default 信息 %}
换行测试
换行测试
换行测试
{% endnotel %}

{% notel blue 提示 %}
换行测试
换行测试
换行测试
{% endnotel %}

{% notel red 自定义标题 %}
换行测试
换行测试
换行测试
{% endnotel %}

### 小提示块

{% note  %}
默认 提示块标签
{% endnote %}

{% note default  %}
default 提示块标签
{% endnote %}

{% note primary  %}
primary 提示块标签
{% endnote %}

{% note success  %}
success 提示块标签
{% endnote %}

{% note info  %}
info 提示块标签
{% endnote %}

{% note warning  %}
warning 提示块标签
{% endnote %}

{% note danger  %}
danger 提示块标签
{% endnote %}

{% note red fa-bolt%}
自定义提示块标签
{% endnote %}



# Buttons 按钮模块

不设置任何参数的 {% btn 按钮:: / %} 适合融入段落中。

regular 按钮适合独立于段落之外：

{% btn regular::示例博客::https://www.ohevan.com::fa-solid fa-play-circle %}

{% btn regular::示例博客::https://www.ohevan.com::fa-solid fa-play-circle %}

large 按钮更具有强调作用，建议搭配 center 使用：

{% btn center large::开始使用::https://redefine-docs.ohevan.com::fa-solid fa-download %}



# Folding 折叠模块

{% folding blue::Folding 测试： 点击查看更多 %}

啊啊啊啊啊

{% note danger  %}
danger 提示块标签
{% endnote %}

{% note tip  %}
tip 提示块标签
{% endnote %}

哈哈哈哈哈哈哈哈哈哈

{% endfolding %}



{% folding pink::测试： 点击查看更多 %}

啦啦啦啦啦啦啦啦啦啦啦啦

{% endfolding %}

```
颜色列表： yellow, blue, green, red, orange, pink, cyan, white, black, gray
```



## 选项卡

{% tabs First unique name %}
<!-- tab First Tab-->
**This is Tab 1.**
<!-- endtab -->

<!-- tab Second Tab-->
**This is Tab 2.**

This is Tab 2.
<!-- endtab -->

<!-- tab Third Tab-->
**This is Tab 3.**

This is Tab 3.

This is Tab 3.
<!-- endtab -->
{% endtabs %}



## 文章自定义

### 首页顶置

```
---
title: Redefine 主题使用指南
date: 2022-9-28 11:45:14
tags: [Hexo]
categories: [Hexo]
sticky: 999
---
```

`sticky` 值越大，顶置的文章越靠前，参考如下

### 首页缩略图

```
---
title: 主题样式 Demo
date: 2022-12-30 19:07:05
tags: "demo"
thumbnail: "https://evan.beee.top/img/208184324-f2640ade-587a-4f46-8ad1-7b4c1b31394f.png"
---
```

### 自定义摘要

```
---
title: Excerpt Test
date: 2022-12-20 12:12:12
tags: Excerpt
categories: Excerpt
excerpt: "这是文章摘要 This is the excerpt of the post"
---
```

