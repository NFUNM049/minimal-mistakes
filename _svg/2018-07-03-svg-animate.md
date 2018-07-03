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
观看动画请点击[佛系三连](http://127.0.0.1:8020/HelloHBuilder/svg04.html)

```
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
``` 


## 2.乱飞的太阳
观看动画请点击[乱飞的太阳](http://127.0.0.1:8020/HelloHBuilder/svg03.html)
```
<?xml version="1.0" encoding="utf-8"?>
<!-- Generator: Adobe Illustrator 21.0.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
		<svg version="1.1" id="图层_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
				 viewBox="0 0 900 500" style="enable-background:new 0 0 900 500;" xml:space="preserve">
			<style type="text/css">
				.st0{fill:#C4FFFD;stroke:#000000;stroke-miterlimit:10;}
				.st1{fill:none;stroke:#000000;stroke-miterlimit:10;}
				.st2{fill:#FFE500;}
				.st3{fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:10;}
				.st4{fill:#FF7C16;}
				.st5{fill:#FF4006;}
			</style>
			<rect y="0" class="st0" width="900" height="500"/>
			<!--<path class="st1" id="line" d="M900,499c-51.6-229.2-261.1-385.1-483.2-369.4C217.1,143.8,44.9,294.2,0,499C0,331,0,163,0-5h900V499z"/>-->
			<g id="sun">
				<circle class="st2" cx="176.8" cy="221.7" r="60.5"/>
				<ellipse class="st2" cx="184.5" cy="133.1" rx="6.1" ry="18.4"/>
				<ellipse class="st2" cx="185" cy="309.3" rx="6.5" ry="16.7"/>
				<ellipse transform="matrix(0.839 -0.5441 0.5441 0.839 -115.6321 178.8174)" class="st2" cx="244.4" cy="284.8" rx="6.4" ry="15.1"/>
				<ellipse transform="matrix(4.710191e-02 -0.9989 0.9989 4.710191e-02 33.7314 478.818)" class="st2" cx="267.8" cy="221.7" rx="6.4" ry="15.4"/>
				<ellipse transform="matrix(4.710191e-02 -0.9989 0.9989 4.710191e-02 -134.4107 294.6794)" class="st2" cx="87.2" cy="217.8" rx="6.2" ry="17.2"/>
				<ellipse transform="matrix(0.839 -0.5441 0.5441 0.839 -63.7336 87.6642)" class="st2" cx="116.3" cy="151.5" rx="6.3" ry="16.9"/>
				<ellipse transform="matrix(0.6384 -0.7697 0.7697 0.6384 -38.4008 248.2698)" class="st2" cx="245" cy="165" rx="15.9" ry="6.4"/>
				<ellipse transform="matrix(0.6384 -0.7697 0.7697 0.6384 -179.4961 189.9759)" class="st2" cx="112.5" cy="286" rx="15.9" ry="6.4"/>
				<ellipse cx="154.8" cy="211" rx="4" ry="7"/>
				<path class="st1" d="M195,210"/>
			<g>
				<polyline class="st3" points="197.3,204 189.3,211 197.3,217.8 	"/>
			</g>
				<ellipse class="st4" cx="141.2" cy="229" rx="7.8" ry="4"/>
				<ellipse class="st4" cx="208.2" cy="229" rx="7.8" ry="4"/>
				<polygon class="st5" points="168.5,240 176.6,247 185.2,240 "/>
				<animatemotion id="sun" path="M900,499c-51.6-229.2-261.1-385.1-483.2-369.4C217.1,143.8,44.9,294.2,0,499C0,331,0,163,0-5h900V499z" begin="0s" dur="8s" rotate="auto" repeatCount="indefinite">
			</g>
		</svg>
```

## 3.会闪的太阳
观看动画请点击[会闪的太阳](http://127.0.0.1:8020/HelloHBuilder/svg01.html)

```
		svg {
			width: 50%;
			height: 50%;
		}
		line {
			stroke-dasharray: 50; 
			stroke-dashoffset: 1000; 
			animation: dash 10s linear both infinite; 
			} 
			@keyframes dash { 
				to { stroke-dashoffset: 0; 
				}
		}
		
		path {
			stroke-dasharray: 1000; 
			stroke-dashoffset: 1000; 
			animation: bash 10s linear both infinite; 
			} 
			@keyframes bash { 
				to { stroke-dashoffset: 0; 
				}
		}
		
		path.sunny {
			stroke-dasharray: 1000; 
			stroke-dashoffset: 1000; 
			animation: bash 50s linear both infinite; 
			} 
			@keyframes bash { 
				to { stroke-dashoffset: 0; 
				}
		}
			
```

## 4.纸飞机飞呀飞
观看动画请点击[纸飞机飞呀飞](http://127.0.0.1:8020/HelloHBuilder/svg02.html)

```
<?xml version="1.0" encoding="utf-8"?>
<!-- Generator: Adobe Illustrator 21.0.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
<svg version="1.1" id="图层_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 900 500" style="enable-background:new 0 0 900 500;" xml:space="preserve">
	 
<style type="text/css">
	.st0{fill:#9FE5FF;}
	.st1{fill:none;stroke:#F2F2F2;stroke-width:3;stroke-miterlimit:10;}
	.st2{fill:none;stroke:#F2F2F2;stroke-width:3;stroke-miterlimit:10;stroke-dasharray:11.9725,11.9725;}
	.st3{fill:#F65229;}
</style>
<rect class="st0" width="900" height="500"/>
<g>
	<g id="Dotted line">
		<!--<path class="st1" d="M67.5,350.6c1.6-1.2,3.3-2.3,4.9-3.5"/>-->
		<path class="st2" d="M82.2,340.3c74.4-51.2,140.3-78.8,188.3-94.7c36.8-12.1,97.8-32.3,105-19c5.4,10.1-19.2,41.3-48,45
			c-35.3,4.5-81.3-32-79-59c6-70.3,347.5-168.7,563-26c29.2,19.3,50.8,39.6,64.8,54.2"/>
		<!--<path class="st1" d="M880.5,245.2c1.5,1.6,2.8,3,4,4.4"/>-->
	</g>
</g>
<g id="cloud">
	<style type="text/css">
	.st7{fill:#9CCBFF;}
	.st8{fill:#B4F9FF;}
	</style>
	<ellipse transform="matrix(0.9992 -3.882057e-02 3.882057e-02 0.9992 -18.6589 23.3339)" class="st7" cx="591.5" cy="492.1" rx="141.5" ry="141.5"/>
	<ellipse transform="matrix(0.9992 -3.882057e-02 3.882057e-02 0.9992 -18.4419 3.6859)" class="st7" cx="85.7" cy="476.7" rx="88.6" ry="88.6"/>
	<ellipse transform="matrix(0.9992 -3.882057e-02 3.882057e-02 0.9992 -15.7434 33.7212)" class="st7" cx="860.4" cy="422.3" rx="30.1" ry="30.1"/>
	<circle class="st8" cx="91.9" cy="500" r="94.8"/>
	<circle class="st8" cx="281.4" cy="435.5" r="124.3"/>
	<circle class="st8" cx="839" cy="539.5" r="124.3"/>
	<circle class="st8" cx="426.4" cy="523.5" r="124.3"/>
	<circle class="st8" cx="608.3" cy="546.5" r="124.3"/>
</g>
<g id="plane">
	<path class="st3" id="plane" d="M31.1,359.7l59.8-9.1l-48.5,16.1L31.1,359.7z M42.7,367.4l48.5-16.1l-42.3,19.4l0.7,14.7L42.7,367.4z"/>
	<path class="st3" id="plane" d="M50.6,388.1l-0.8-14.7l10.5,6.7L50.6,388.1z M68.1,383.7l-8-5.2l-10.5-6.7l42.3-19.4L68.1,383.7z"/>
    <animateMotion id="plane" path="M82.2,340.3c74.4-51.2,140.3-78.8,188.3-94.7c36.8-12.1,97.8-32.3,105-19c5.4,10.1-19.2,41.3-48,45
			c-35.3,4.5-81.3-32-79-59c6-70.3,347.5-168.7,563-26c29.2,19.3,50.8,39.6,64.8,54.2" begin="0s" dur="10s" rotate="auto" repeatCount="indefinite">
  
</g>
</svg>
```