---
title:  "svg的基本说明"
categories: 
  - 网页设计
tags:
  - svg
classes: wide
excerpt: "svg基本信息"
header:
  overlay_image: /images/boy and sea.jpg
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
# cta_label: "More Info"
# cta_url: "https://unsplash.com"
---

{% include base_path %}

{% include toc title="目录" %}

SVG 全称是 Scalable Vector Graphics，即矢量图，可以解决位图放大失真的问题。我们要把 SVG 和 CSS，Canvas，HTML 分清楚。Canvas提供的功能更原始，适合像素处理，动态渲染和大数据量绘制；**SVG 是通过 XML 的形式写在 HTML 文档中的，而且功能更完善，适合静态图片展示。**

## svg的优势：
* 比起JPEG格式，它的尺寸更小，且压缩性更强。
* 高保真，高质量。
* 可以被很多工具读取。
* 可伸缩。
* 它采用文本来描述图像。

## svg形状
* 矩形 <rect>
* 圆形 <circle>
* 椭圆 <ellipse>
* 线 <line>
* 折线 <polyline>
* 多边形 <polygon>
* 路径 <path>

## svg渐变
SVG 渐变必须在 <defs> 标签中进行定义。
1.线性渐变<linearGradient>
2.放射渐变<radialGradient> 

##svg动画
我们如果想实现一个动画效果，可以通过css和js实现。
另一种方法是直接使用svg自带的动画属性animate，这个方法会更加的便利和简单。
[svg动画例子](https://www.villainhr.com/page/2017/05/01/SVG%20%E5%8A%A8%E7%94%BB%E7%B2%BE%E9%AB%93)
