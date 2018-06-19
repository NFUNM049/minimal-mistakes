---
title:  "svg的历史"
categories: 
  - 网页设计
tags:
  - svg
---

{% include base_path %}

{% include toc title="Getting Started" %}

SVG 全称是 Scalable Vector Graphics，即矢量图，可以解决位图放大失真的问题。我们不要把 SVG 和 CSS，Canvas，HTML 搞混。Canvas提供的功能更原始，适合像素处理，动态渲染和大数据量绘制；**SVG 是通过 XML 的形式写在 HTML 文档中的，而且功能更完善，适合静态图片展示，高保真文档查看和打印的应用场景。**

##一、三种把 SVG 文件嵌入 HTML 页面的不同方法。
* 使用<embed>、<object> 或者 <iframe>。

##二、svg形状
* 矩形 <rect>
* 圆形 <circle>
* 椭圆 <ellipse>
* 线 <line>
* 折线 <polyline>
* 多边形 <polygon>
* 路径 <path>

##svg滤镜
* feBlend
* feColorMatrix
* feComponentTransfer
* feComposite
* feConvolveMatrix
* feDiffuseLighting
* feDisplacementMap
* feFlood
* feGaussianBlur
* feImage
* feMerge
* feMorphology
* feOffset
* feSpecularLighting
* feTile
* feTurbulence
* feDistantLight
* fePointLight
* feSpotLight

##二、svg渐变
**SVG 渐变必须在 <defs> 标签中进行定义。**
1.线性渐变<linearGradient>
2.放射渐变<radialGradient> 

##svg动画
[svg动画例子](https://www.villainhr.com/page/2017/05/01/SVG%20%E5%8A%A8%E7%94%BB%E7%B2%BE%E9%AB%93)
