<template>
	<div id="index">
		
		<web-header></web-header>
		<carousel-map type="turnBox"></carousel-map>
		<div class="area values">
			<div class="title">
				<h1>核心<span>价值观</span></h1>
				<img src="../../static/imgs/areaHeader-icon.png" alt="">
				<p>每个校园都是按照国际纯正蒙台梭利校园的特点和标准精心设计的，充满着温馨关爱的教育氛，打造了最适合孩子健康成长的校园环境。</p>
			</div>
			<div class="content">
				<ul class="clearfix">
					<li><img src="../../static/imgs/first-1.png" alt="">智能课程</li>
					<li><img src="../../static/imgs/first-2.png" alt="">智能课程</li>
					<li><img src="../../static/imgs/first-3.png" alt="">智能课程</li>
					<li><img src="../../static/imgs/first-4.png" alt="">智能课程</li>
				</ul>
			</div>
		</div>
		<div class="area about">
			<div class="content">
				<h1>关于我们</h1>
				<p>东方幼儿园创办于1992年9月，一园四址规模， 42个班级，一千多名幼儿,教职工220名。东方幼儿园在育人环境上充分体现尊重与关爱儿童的理念，每处园所构思新颖、独具一格，均设有大型室内溜冰场、室内温水游泳池、大型运动器具、翻斗乐、玩沙池、植物园、浴室、洗衣房等，有设备先进的科技活动室、舞蹈房、建构室、围棋室、图书室、电脑室、钢琴房、古筝室、手风琴房等。</p>
			</div>
		</div>
		<div class="area course buttonWave">
			<div class="title">
				<h1>特色<span>课程</span></h1>
				<img src="../../static/imgs/areaHeader-icon.png" alt="">
				<p>每个校园都是按照国际纯正蒙台梭利校园的特点和标准精心设计的，充满着温馨关爱的教育氛，打造了最适合孩子健康成长的校园环境</p>
			</div>
			<div class="content">
				<ul class="clearfix">
					<li>
						<h4>美术<span>FINE ARTS</span></h4>
						<p>关于儿童美术教育的核心理念，朱敬一- 知名艺术家，艺术普及专家提出了“感知力是美学的第一要义”这个观点。</p>
						<button>查看更多</button>
					</li>
					<li>
						<h4>美术<span>FINE ARTS</span></h4>
						<p>关于儿童美术教育的核心理念，朱敬一- 知名艺术家，艺术普及专家提出了“感知力是美学的第一要义”这个观点。</p>
						<button>查看更多</button>
					</li>
					<li>
						<h4>美术<span>FINE ARTS</span></h4>
						<p>关于儿童美术教育的核心理念，朱敬一- 知名艺术家，艺术普及专家提出了“感知力是美学的第一要义”这个观点。</p>
						<button>查看更多</button>
					</li>
					<li>
						<h4>美术<span>FINE ARTS</span></h4>
						<p>关于儿童美术教育的核心理念，朱敬一- 知名艺术家，艺术普及专家提出了“感知力是美学的第一要义”这个观点。</p>
						<button>查看更多</button>
					</li>
				</ul>
			</div>
		</div>
		<div class="area welcome bottomWave">
			<div class="title">
				<img src="../../static/imgs/welcome.png" alt="">
				<h1>欢迎来到EDUCATION幼儿园</h1>
				<p>每个校园都是按照国际纯正蒙台梭利校园的特点和标准精心设计的，充满着温馨关爱的教育氛，打造了最适合孩子健康成长的校园环境</p>
			</div>
			<div class="content">
				<ul class="clearfix">
					<li><img src="../../static/imgs/welcome-1.png" alt="">健康的饮食</li>
					<li><img src="../../static/imgs/welcome-2.png" alt="">健康的饮食</li>
					<li><img src="../../static/imgs/welcome-3.png" alt="">健康的饮食</li>
					<li><img src="../../static/imgs/welcome-4.png" alt="">健康的饮食</li>
				</ul>
				<button>我要预约</button>
			</div>
		</div>
		<div class="area teaching buttonWave">
			<div class="title">
				<h1>特色<span>课程</span></h1>
				<img src="../../static/imgs/areaHeader-icon.png" alt="">
				<p>每个校园都是按照国际纯正蒙台梭利校园的特点和标准精心设计的，充满着温馨关爱的教育氛，打造了最适合孩子健康成长的校园环境</p>
			</div>
			<div class="content">
				<ul class="clearfix">
					<li class="mr15"><img src="../../static/imgs/teaching-1.jpg" alt=""></li>
					<li class="col2"><img src="../../static/imgs/teaching-2.jpg" alt=""></li>
					<li class="mr15"><img src="../../static/imgs/teaching-3.jpg" alt=""></li>
					<li class="mr15"><img src="../../static/imgs/teaching-4.jpg" alt=""></li>
					<li><img src="../../static/imgs/teaching-5.jpg" alt=""></li>
				</ul>
			</div>
		</div>
		<pub-footer></pub-footer>
	</div>
</template>

<script>
import webHeader from '@/components/webHeader'
import carouselMap from '@/components/carouselMap' //* 可选属性 type(过渡类型)：turnBox(翻转盒子), dalay(自动播放时间间隔): number, isPoint(小黑点): Bollean
import areaHeader from '@/components/areaHeader'
import pubFooter from '@/components/pubFooter'
export default {
	components: { webHeader, pubFooter, carouselMap, areaHeader }
}
</script>

<style lang="scss">
#index {
	min-width: 1200px;
	.buttonWave {
		background: url(../../static/imgs/background-1.png) 0 bottom/20px 110px repeat-x;
	}
	.values {
		z-index: 1;
		background:  url(../../static/imgs/background-2.png) 0 top/20px 110px repeat-x;
		margin-top: -20px;
	}
	.area {
		float: left;
		width: 100%;
		position: relative;
		z-index: 1;
		.title {
			text-align: center;
			margin: 60px 0 20px;
			h1 {
				line-height: 64px;
				font-size: 36px;
				span {
					color: #FF6537;
				}
			}
			img {
				margin-bottom: 1.2em;
			}
			p {
				width: 680px;
				margin: 0 auto;
				line-height: 2;
				font-size: 14px;
			}
		}
		.content {
			ul {
				width: 1200px;
				margin: 0 auto;
				li {
					float: left;
					text-align: center;
					width: 25%;
					font-size: 1.2em;
					line-height: 4;
					img {
						display: block;
						margin: 0 auto;
					}
				}
			}
		}
	}
	.about {
		margin-top: 40px;
		height: 600px;
		position: relative;
		background: url(../../static/imgs/about.jpg) -240px 0/cover no-repeat;
		.content {
			position: absolute;
			top: 130px;
			left: 550px;
			width: 650px;
			h1 {
				color: #FF6537;
				line-height: 3;
			}
			p {
				font-size: 14px;
				color: #888;
				line-height: 1.8;
			}
		}
	}
	.course {
		.content {
			ul {
				margin-top: 30px;
				li {
					float: left;
					width: 574px;
					height: 233px;
					margin-bottom: 20px;
					padding-left: 264px;
					padding-right: 10px;
					text-align: left;
					box-sizing: border-box;
					&:nth-child(2n - 1) {
						margin-right: 52px;
					}
					h4 {
						font-weight: normal;
						line-height: 2;
						margin-top: 30px;
						color: #FF6537;
						span {
							color: #999;
							margin-left: 10px;
							font-size: 14px;
						}
					}
					p {
						font-size: 14px;
						line-height: 1.7;
						color: #555;
						height: 75px;
					}
					button {
						border-radius: 30px;
						border: none;
						padding: 12px 40px;
						color: #fff;
					}
					&:nth-child(1) {
						background: url(../../static/imgs/course-1.jpg) 0 0/100% 100% no-repeat;
						button {
							background-color: #625bbc;
						}
					}
					&:nth-child(2) {
						background: url(../../static/imgs/course-2.jpg) 0 0/100% 100% no-repeat;
						button {
							background-color: #ff6537;
						}
					}
					&:nth-child(3) {
						background: url(../../static/imgs/course-3.jpg) 0 0/100% 100% no-repeat;
						button {
							background-color: #49cad9;
						}
					}
					&:nth-child(4) {
						background: url(../../static/imgs/course-4.jpg) 0 0/100% 100% no-repeat;
						button {
							background-color: #2ac756;
						}
					}
				}
			}
		}
	}
	.welcome {
		color: #fff;
		margin-top: -10px;
		z-index: 0;
		background: url(../../static/imgs/welcomeBg.jpg) 0 0/100% 100% no-repeat;
		.content {
			text-align: center;
			button {
				border-radius: 30px;
				border: none;
				background-color: #ff6537;
				height: 54px;
				width: 226px;
				line-height: 54px;
				font-size: 18px;
				margin-bottom: 30px;
				color: #fff;
			}
		}
	}
	.teaching {
		.content {
			margin-bottom: 80px;
			ul {
				li {
					overflow: hidden;
					width: 390px;
					margin-top: 15px;
					&:hover {
						img {
							transform: scale(1.2)
						}
					}
					img {
						width: 100%;
						height: 296px;
						transition: all .2s;
					}
				}
				.mr15 {
					margin-right: 15px;
				}
				.col2 {
					width: 795px;
				}
			}
		}
	}
}
</style>

