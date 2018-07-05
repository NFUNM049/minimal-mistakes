---
title:  "svg动画"
categories: 
  - 网页设计
tags:
  - svg
classes: wide
excerpt: "尝试用svg制作动画"
header:
  overlay_image: /images/tree.png
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
# cta_label: "More Info"
# cta_url: "https://unsplash.com"
---

{% include base_path %}

{% include toc title="目录" %}

>SVG 是基于 XML 的矢量图形描述语言，所以能和 JS 以及 CSS 进行交互。 特别是 CSS，配合 CSS Animation 就能实现一些令人心旷神怡的动画，这实在是让人兴奋。下面我们就来看看 SVG 配合 CSS 实现动画的一些方法。

## 1.佛系三联
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<svg width="1000" height="320" xmlns="http://www.w3.org/2000/svg">
          <g> 
              <text font-family="microsoft yahei" font-size="120" y="160" x="160">
    		  好
              <animate attributeName="x" from="60" to="160" begin="0s" dur="2s" repeatCount="indefinite" />
              <animateTransform attributeName="transform" begin="0s" dur="2s" type="scale" from="1" to="1.5"  repeatCount="indefinite" />
              <animate attributeName="opacity" begin="0s" dur="2s" from="1" to="0" repeatCount="indefinite" />
    </text>
         </g>
</svg>

 		<svg width="1000" height="320" xmlns="http://www.w3.org/2000/svg">
          <g> 
              <text font-family="microsoft yahei" font-size="60" y="160" x="160">
    		  我知道了
              <animate attributeName="x" from="60" to="160" begin="0s" dur="2s" repeatCount="indefinite" />
              <animateTransform attributeName="transform" begin="0s" dur="2s" type="scale" from="1" to="1.5"  repeatCount="indefinite" />
              <animate attributeName="opacity" begin="0s" dur="2s" from="1" to="0" repeatCount="indefinite" />
    </text>
         </g>
</svg>

		<svg width="1000" height="320" xmlns="http://www.w3.org/2000/svg">
          <g> 
              <text font-family="microsoft yahei" font-size="60" y="160" x="160">
    		  你说什么都对
              <animate attributeName="x" from="60" to="160" begin="0s" dur="2s" repeatCount="indefinite" />
              <animateTransform attributeName="transform" begin="0s" dur="2s" type="scale" from="1" to="1.5"  repeatCount="indefinite" />
              <animate attributeName="opacity" begin="0s" dur="2s" from="1" to="0" repeatCount="indefinite" />
    </text>
         </g>
</svg>
	</body>
</html>

