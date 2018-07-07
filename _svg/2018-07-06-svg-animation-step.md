---
title:  "svg动画制作的基本步骤"
categories: 
  - 网页设计
tags:
  - svg
classes: wide
excerpt: "svg动画制作的基本步骤和思路"
header:
  overlay_image: /images/SVG.jpg
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
# cta_label: "More Info"
# cta_url: "https://unsplash.com"
sidebar:
  nav: "docs"
---

{% include base_path %}

{% include toc title="目录" %}


### svg动画制作的基本步骤

基本思路是首先是将svg代码放入body里，然后用css动画代码或svg animate命令其动。

在这门作业里，我是另外在hbuilder新建了一个HTML档，然后在这里写可以实时观察动画情况，当动画写好之后，再把代码复制到md文章之中！然后你就可以看到你网站里的svg动画啦！

首先，我们每一个svg动画都需要有这些代码。

```
<?xml version="1.0" xmlns="http://www.w3.org/2000/svg" viewport="0 0 900 500" >
```
version： svg 的版本，目前只有 1.0，1.1 两种。
xmlns：http://www.w3.org/2000/svg 为固定值。
xmlns:xlink：http://www.w3.org/1999/xlink 为固定值。

然后，第二步，我们通过ai软件或svg的[在线编辑器](http://www.zuohaotu.com/svg/)(个人觉得这个还挺方便的)画出我们所需要的图形。如果是简单的正方形、长方形、圆形、路径，我们也可以自己简单的实现它。

以下使用在线编辑器进行举例。

##  一，打开编辑器，画出你想要的图形，填充颜色。这一步里，需要注意的是要设置好画布大小。

![Svg animation step 1.png](https://upload-images.jianshu.io/upload_images/9455364-87fd3e4b798ad4d9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 二，画好自己满意的图形后点击左上角文件-保存，它会自动保存为svg图。

![Svg animation step 2.png](https://upload-images.jianshu.io/upload_images/9455364-b43d27d95ceb7bc7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 三，打开你刚刚保存的svg图，它会用浏览器打开。

![Svg animation step 3.png](https://upload-images.jianshu.io/upload_images/9455364-dc07df4b5017f387.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 四，右键查看源代码！恭喜你，这就是你刚刚所做的图形的svg代码啦！

![Svg animation step 4.png](https://upload-images.jianshu.io/upload_images/9455364-dfeb57a924d343de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 五，在你喜欢的编辑器里新建一个HTML文件，然后把svg源代码全部复制至body中。Ctrl+s保存，右边就会出现你刚刚画的图啦。接下来就是你的脑洞创造啦~

![Svg animation step 5.png](https://upload-images.jianshu.io/upload_images/9455364-7dabab331dd78255.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

插入svg图的代码后，我们就可以命令它动啦！

无论是让他转圈圈，左右上下溜达，还是让他飞起来，你都可以通过代码去实现！