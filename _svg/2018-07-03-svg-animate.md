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
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
		
		</style>
	</head>
	<body>
		
	<?xml version="1.0" standalone="no"?>
	<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
	<svg t="1530888404261" class="icon" style="" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2380" xmlns:xlink="http://www.w3.org/1999/xlink" width="200" height="200">
		
		<defs><style type="text/css"></style></defs>
		
				<path id="bg" d="M892.1 288.6v612.2c0 15.2-12.3 27.4-27.4 27.4H230.5c-11.5 
				0-20.9-9.3-20.9-20.9V79.5c0-8.4 6.8-15.3 15.3-15.3h427.4c0.9 0 1.3 
				1 0.7 1.7-0.4 0.4-0.4 1 0.1 1.4l238.7 220.5c0.2 0.3 0.3 0.5 0.3 0.8z" 
				fill="#0B1C24" p-id="2381">
				<animateTransform 
		             attributeName="transform"
		             type="scale"
		             values="1;1.1;1"
		             keyTimes="0;0.5;1"
		             begin="0" dur="1.5s" repeatCount="indefinite"
		             fill="freeze"></animate>
				</path>
			
				<path id="line" d="M541.7 384.7h-466c-7.3 0-13.2-5.9-13.2-13.2v-178c0-7.3 
				5.9-13.2 13.2-13.2h466c7.3 0 13.2 5.9 13.2 13.2v178c0 7.3-5.9 13.2-13.2 
				13.2zM652.5 273.8V64.2l239.7 223.9H666.8c-7.9 0.1-14.3-6.4-14.3-14.3z" 
				fill="#4FC1FF" 
				p-id="2382">
				<animateTransform 
		             attributeName="transform"
		             type="scale"
		             values="1;1.1;1"
		             keyTimes="0;0.5;1"
		             begin="0" dur="1.5s" repeatCount="indefinite"
		             fill="freeze"></animate>
				</path>
				
				<path d="M214.1 294.2V321h-16.4v-76.9h26.5c19.1 0 
				28.7 8.1 28.7 24.3 0 7.9-2.9 14.2-8.7 18.9-5.8 4.8-13 7-21.7 6.8h-8.4z 
				m0-37.4v24.8h7.1c9.6 0 14.5-4.2 14.5-12.6 0-8.2-4.8-12.3-14.3-12.3h-7.3zM261 
				301.6c6.2 5.1 13.2 7.7 21.1 7.7 4.5 0 7.8-0.8 10.1-2.3 2.3-1.5 3.4-3.5 
				3.4-5.9 0-2.1-0.9-4.1-2.7-5.9-1.8-1.9-6.5-4.4-14.2-7.5-12-5.1-18-12.5-18-22.2 
				0-7.2 2.7-12.7 8.2-16.7 5.4-4 12.7-5.9 21.6-5.9 7.5 0 13.8 1 18.9 
				2.9v15.4c-5.2-3.5-11.2-5.3-18.1-5.3-4 0-7.3 0.7-9.7 2.2-2.4 1.5-3.6 
				3.5-3.6 5.9 0 2 0.8 3.8 2.5 5.5 1.7 1.7 5.7 3.9 12.3 6.8 7.6 3.3 12.9 
				6.7 15.8 10.4 2.9 3.6 4.3 8 4.3 13 0 7.4-2.6 13-7.8 16.9-5.2 3.9-12.7 
				5.8-22.3 5.8-8.8 0-16-1.4-21.7-4.3v-16.5zM325.7 321v-76.9h26.6c27.3 0 
				41 12.5 41 37.5 0 11.9-3.8 21.4-11.5 28.6-7.6 7.2-17.5 10.8-29.6 10.8h-26.5z 
				m16.4-63.5v50.1h8.9c7.8 0 13.9-2.3 18.3-7 4.4-4.6 6.7-10.9 
				6.7-18.8 0-7.6-2.3-13.6-7-17.9-4.6-4.3-10.7-6.4-18.1-6.4h-8.8z" 
				fill="" p-id="2383">
				<animate attributeName="opacity" begin="0s" dur="3s" values="1;0;1"
		             keyTimes="0;0.5;1" repeatCount="indefinite" />
				</path>
				
				<path id="ps" d="M449.2 677.6V759h-44.8V525.4h72.4c52.3 0 78.5 24.6 78.5 73.9 0 
					23.9-7.9 43.1-23.7 57.5-15.8 14.4-35.6 21.3-59.3 20.7h-23.1z m0-113.6v75.4h19.4c26.3 
					0 39.5-12.7 39.5-38.2 0-24.8-13-37.2-39.1-37.2h-19.8zM578.8 714.2c15 10.2 
					29.7 15.2 44.1 15.2 18.1 0 27.2-5.4 27.2-16.1 
					0-7.6-7.5-14-22.4-19.2-18.6-6.4-31.5-13.6-38.4-21.5-7-7.9-10.5-18.6-10.5-32 0-16.4 
					6-29.2 17.9-38.5 11.9-9.3 27.6-13.9 47-13.9 13.8 0 27 2.3 
					39.8 6.8v38.3c-11.7-7.6-24.5-11.5-38.6-11.5-7 0-12.6 1.4-16.8 
					4.1-4.3 2.8-6.4 6.4-6.4 10.9 0 7.6 6.3 13.8 19 18.5 13.6 5 
					23.8 9.6 30.6 13.7 6.8 4.1 12 9.6 15.6 16.3 3.6 6.7 5.4 14.5 
					5.4 23.4 0 17.2-6.2 30.5-18.6 40-12.4 9.5-29 14.3-49.7 14.3-16.3 
					0-31.4-2.9-45.2-8.6v-40.2z" fill="#4FC1FF" p-id="2384">
					<animateTransform 
		             attributeName="transform"
		             type="scale"
		             values="1;0.9;1"
		             keyTimes="0;0.5;1"
		             begin="0" dur="1.5s" repeatCount="indefinite"
		             fill="freeze"></animate>
			    </path>
		</svg>
	</body>
</html>


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



