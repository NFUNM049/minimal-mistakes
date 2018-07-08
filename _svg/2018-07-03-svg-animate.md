---
title:  "svg动画"
categories: 
  - 网页设计
tags:
  - svg
classes: wide
excerpt: "尝试用svg制作动画"
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

>SVG 是基于 XML 的矢量图形描述语言，所以能和 JS 以及 CSS 进行交互。 特别是 CSS，配合 CSS Animation 就能实现一些令人心旷神怡的动画，这实在是让人兴奋。下面我们就来看看 SVG 配合 CSS 实现动画的一些方法。

## 佛系三联
做这个的时候本来是尝试着用文字试试做动画，看看会不会动，结果出乎意料的懂动了！然后我又尝试使用另外两种动画，即缩放和透明度的变换。总结：做这个还蛮顺利的。
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

## 活奔乱跳的PS
做这个的话其实没有达到我想要的效果，我原本想的是ps两个字母从上面掉下来然后弹两下后弹回原位。有想法但是做不出！所以只能做简单一点的了。
(不知道为啥放不上来？)
[点击查看动画](http://127.0.0.1:8020/HelloHBuilder/svg09.html)

## 会闪的太阳
这个是我的svg动画的第一个作品，有点拙劣。不过能动就让我很开心啦！第一次制作动画，我学会了使用stroke-dasharray、stroke-dashoffset这两个属性，通过它们我们可以制作出有趣的线条动画。
			
<html>
	<head>
		<title></title>
		<style>
			
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
			

		</style>
	</head>
	<body>
		<?xml version="1.0" encoding="utf-8"?>
		<!-- Generator: Adobe Illustrator 21.0.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
		<svg version="1.1" id="图层_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
		 viewBox="0 0 128 128" style="enable-background:new 0 0 128 128;" xml:space="preserve">
			
			<style type="text/css">
				.st0{fill:#FFFFFF;stroke:#F7931E;stroke-miterlimit:10;}
				.st1{fill:none;stroke:#F7931E;stroke-miterlimit:10;}
				.st2{fill:none;stroke:#C1272D;stroke-miterlimit:10;}
			</style>
			
			<path class="st0" d="M82.6,53.7c0,12.3-9.9,22.2-22.2,22.2s-22.2-9.9-22.2-22.2s9.9-22.2,22.2-22.2c5.4,0,9.4,2,10.7,2.8
				C77.8,38,82.6,45.5,82.6,53.7z"/>
			<path class="st0" d="M69.9,33.6c-8.6-1.7-17.1,1.6-21.3,8.2c-5.8,9-2.4,22.6,6.9,27.1c6.7,3.3,17,2.1,21.4-5.2
				c5-8.2-0.1-20.2-8.1-22.9c-5.3-1.7-13.2,0.3-15.2,5.6c-1.5,3.8-0.1,9.8,3.8,11.1c3.4,1.1,8.4-1.6,8.7-5.3c0.2-2.9-2.6-5.1-2.9-5.3"
				/>
			<!--<line class="st1" stroke-linecap='round' x1="53" y1="16.9" x2="54.3" y2="26"/>-->
			<line class="st1" stroke-linecap='round' x1="54.3" y1="26" x2="53" y2="16.9"/>
			<line class="st1" stroke-linecap='round'  x1="68.6" y1="80.6" x2="71.1" y2="90.5"/>
			<line class="st1" stroke-linecap='round'  x1="73.9" y1="30.4" x2="80.1" y2="21.5"/>
			<line class="st1" stroke-linecap='round'   x1="51" y1="79.3" x2="47.2" y2="88.9"/>
			<line class="st1" stroke-linecap='round'  x1="51" y1="79.3" x2="47.2" y2="88.9"/>
			<line class="st1" stroke-linecap='round'   x1="86.4" y1="41.1" x2="97.5" y2="39.4"/>
			<line class="st1" stroke-linecap='round'   x1="37.6" y1="69.7" x2="27" y2="75.1"/>
			<!--<line class="st1" stroke-linecap='round'   x1="30.5" y1="24.4" x2="38.9" y2="33.2"/>-->
			<line class="st1" stroke-linecap='round'   x1="38.9" y1="33.2" x2="30.5" y2="24.4"/>
			<line class="st1" stroke-linecap='round'   x1="79.9" y1="71.3" x2="88.8" y2="81"/>
			<line class="st1" stroke-linecap='round'   x1="87.6" y1="58.2" x2="100.9" y2="58.9"/>
			<line class="st1" stroke-linecap='round'   x1="32.3" y1="51.4" x2="20.1" y2="50.9"/>
			<path class="st2 sunny" d="M42.1,99.6c-1.2,0.9-2.5,2-2.2,2.8c0.4,1.2,3.7,0.6,4.2,1.8c0.3,0.6-0.2,1.8-3.2,4.2"/>
			<path class="st2 sunny" d="M48.6,99.5c0,0.5,0,4.1,0.3,6.6c0,0.4,0.1,1,0.7,1.4c0.5,0.4,1.4,0.5,2,0.3c1.1-0.4,1.3-1.7,1.5-3.1
				c0.2-1.1,0.2-2.8-0.4-4.9"/>
			<path class="st2 sunny" d="M57.7,107.9c0.7-3,0.5-4.9,0.2-6.1c-0.1-0.3-0.3-0.8,0-1.3c0.6-0.8,2.6-0.7,3.6,0.1c1.3,1.1,1.1,4-0.8,7.1"/>
			<path class="st2 sunny" d="M67,107.1c-0.4-2.9-0.8-4.9-1.1-6.6c-0.1-0.6-0.3-1.4,0.2-1.8c0.6-0.6,2.2-0.1,3,0.5c2.5,1.8,1.3,7.1,1.2,7.5"
				/>
			<path class="st2 sunny" d="M74.6,99.2c0,4.1,0.9,6.9,2,7.1c0.7,0.1,1.9-0.7,2.5-1.6c0.1-0.1,0.3-0.4,0.5-0.8c0.2-0.4,0.4-1.2,0.3-2.4
				c-0.1-1.5-0.6-2.5-0.6-2.5c0,0,1.3,2.7,1.6,6.4c0.1,2,0.2,4.4-1.3,5.4c-1,0.7-2.2,0.5-2.9,0.4"/>
			</svg>
	</body>
</html>

## 乱飞的太阳
在这个动画中，我遇到了些困难————太阳没有按我给的路径飞！！！我确认过很多次，路径是没有错的，但是太阳就是瞎飞飞，可能它有自己的理想吧......
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
				<style>
			svg {
				width: 60%;
				height: 50%;
			}
		</style>
	</head>
	<body>
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

	</body>
</html>

## 先转几圈然后再走的方形

虽然这个动画挺无聊，但我学会了如何让动画做完一个效果之后紧接着做下一个效果，即begin="c1.end+1.5s"。

<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
	
<svg xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink" viewport="0 0 1000 1000" height="100" width="300">

    <rect x="50" y="50" height="110" width="110"
         style="fill: #656524">
        <animateTransform
        	id="first"
            attributeName="transform"
            begin="0s"
            dur="3s"
            type="rotate"
            from="0 105 105"
            to="360 105 105"
            repeatCount="1"
            fill="freeze"
        />
        <animate attributeName="x" from="-60" to="300" 
        	begin="first.end" dur="2s" repeatCount="indefinite" />
    </rect>
	</body>
</html>

## 怦然心动

怦怦乱跳的心

<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
<svg width="800" height="600" xmlns="http://www.w3.org/2000/svg">
 <!-- Created with Method Draw - http://github.com/duopixel/Method-Draw/ -->
	 <g>
	  	<title>background</title>
	  	<g display="none" overflow="visible" y="0" x="0" height="100%" width="100%" id="canvasGrid">
	   <rect fill="url(#gridpattern)" stroke-width="0" y="0" x="0" height="100%" width="100%"/>
	 	</g>
	 </g>
	 <g>
	  <title>Layer 1</title>
	  <path stroke="#fcfcf9" id="svg_1" d="m399.999992,263.164109c30.3037,-83.87237 149.034589,0 0,107.835904c-149.034589,-107.835904 -30.3037,-191.708273 0,-107.835904z" stroke-width="0" fill="#ff0f5b"/>
  		<animateTransform 
             attributeName="transform"
             type="scale"
             values="1;1.5;1"
             keyTimes="0;0.2;1"
             calcMode="spline" keySplines=".5 0 .5 1;.5 0 .5 1"
             begin="0" dur="1.5s" repeatCount="indefinite"
             fill="freeze"></animate>
 </g>
</svg>
	</body>
</html>

## star

一边转一边闪

<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<div>
			<svg width="800" height="600" xmlns="http://www.w3.org/2000/svg">
			 <!-- Created with Method Draw - http://github.com/duopixel/Method-Draw/ -->
				 <g>
					  <title>background</title>
					  <g display="none" overflow="visible" y="0" x="0" height="100%" width="100%" id="canvasGrid">
					   <rect fill="url(#gridpattern)" stroke-width="0" y="0" x="0" height="100%" width="100%"/>
					  </g>
				 </g>
				 <g>
				  	<title>Layer 1</title>
				 	 <path stroke="#ffffff" id="svg_1" d="m1.2325,75.947817l75.368451,0l23.289431,-74.483575l23.289445,74.483575l75.368438,0l-60.974246,46.032854l23.290636,74.483575l-60.974273,-46.034107l-60.97426,46.034107l23.290643,-74.483575l-60.974266,-46.032854z" stroke-width="1.5" fill="#fcc567"/>
				 	<animateTransform
				 		attributeName="transform"
				 		begin="0s"
				 		dur="5s"
				 		type="rotate"
				 		from="0 100 100"
				 		to="360 100 100"
				 		repeatCount="indefinite"
				 		/>
				 	
				 	<animate attributeName="opacity" begin="0s" dur="2s" values="1;0;1" repeatCount="indefinite" />
				 	
				 </g>
			</svg>
		</div>
	</body>
</html>