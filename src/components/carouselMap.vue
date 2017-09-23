<template>
	<div id="carouselMap">
		<div class="imgList">
			<transition :name="myType">
				<img :src="img" v-for="(img, imgIndex) in imgs" :key="imgIndex" v-if="active === imgIndex">
				<!-- <img :src="imgs[active]"> -->
			</transition>
		</div>
		<div class="handel">
			<div class="point" v-if="isPoint" @mouseout="autoPlay()">
				<div 
				:class="pointIndex === active ? 'round active' : 'round'" 
				v-for="(point, pointIndex) in imgs" 
				:key="pointIndex"
				@click="active = pointIndex"
				@mouseover="stopPlay(pointIndex)"
				></div>
			</div>
			<div class="handler">
				<div class="left" @click="changeBanner(-1)">
					<svg class="icon" aria-hidden="true">
						<use xlink:href="#icon-lt"></use>
					</svg>
				</div>
				<div class="right" @click="changeBanner(1)">
					<svg class="icon" aria-hidden="true">
						<use xlink:href="#icon-gt"></use>
					</svg>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			isPoint: true,
			active: 0,
			imgs: [
				'../../static/imgs/banner1.png',
				'../../static/imgs/banner2.jpg',
				'../../static/imgs/banner3.jpg'
			],
			timer: '',
			myType: this.type
		}
	},
	watch: {
		active(val, old) {
			if (old > val && this.type === 'turnBox') {
				this.myType = 'turnBox-turnBack';
			} else if (this.myType === 'turnBox-turnBack') {
				this.myType = 'turnBox';
			}
			if (this.active < 0) {
				this.active = this.imgs.length - 1;
			}
			if (this.active >= this.imgs.length) {
				this.active = 0;
			}
		}
	},
	methods: {
		changeBanner(i) {
			this.active += i;
			this.autoPlay();
		},
		stopPlay(i) {
			clearInterval(this.timer);
			this.active = i;
		},
		autoPlay() {
			clearInterval(this.timer);
			// this.timer = setInterval(() => {
			// 	this.active++;
			// }, this.dalay * 1000);
		}
	},
	created() {
		this.autoPlay();
	},
	props: {
		type: {
			type: String,
			default: 'fade'
		},
		dalay: {
			type: Number,
			default: 3
		}
	}

}
</script>

<style lang="scss" scoped>
#carouselMap {
	position: relative;
	min-width: 1200px;
	height: 680px;
	.imgList {
		height: 100%;
		width: 100%;
		min-width: 1200px;
		overflow: hidden;
		white-space: nowrap;
		position: relative;
    perspective: 2000px;
		img {
			position: absolute;
			left: 0;
			top: 0;
			width: 100%;
			height: 680px;
		}
	}
	.handel {
		.point {
			position: absolute;
			left: 50%;
			bottom: 10px;
			transform: translateX(-50%);
			.round {
				width: 12px;
				height: 12px;
				background-color: #000;
				opacity: .7;
				border-radius: 50%;
				float: left;
				margin: 0 10px;
				&:hover {
					opacity: 1;
				}
			}
			.active {
				opacity: 1;
			}
		}
		.handler {
			&>div {
				position: absolute;
				top: 50%;
				background-color: rgba(0, 0, 0, .3);
				text-align: center;
				height: 60px;
				width: 60px;
				line-height: 82px;
				border-radius: 8px;
				transform: translateY(-50%);
				cursor: pointer;
				&:hover{
					background-color: rgba(0, 0, 0, .8);
				}
				.icon {
					height: 40px;
					width: 40px;
				}
			}
			.left {
				left: 10px;
			}
			.right {
				right: 10px;
			}
		}
	}


//* 动画类型


//* 渐隐(默认)
	.fade-enter-active, .fade-leave-active {
		transition: opacity 1s
	}
	//* 离开状态
	.fade-leave-to, .fade-enter {
		opacity: 0;
	}

//翻转盒子
	//* 过度过程 可以用来定义时间、延迟和曲线函数
	.turnBox-enter-active, .turnBox-leave-active, .turnBox-turnBack-enter-active, .turnBox-turnBack-leave-active {
		backface-visibility: hidden;
		transition: transform 1s;
	}

	//* 离开状态
	.turnBox-leave-to {
		transform: rotateX(90deg);
		transform-origin: 50% 50% -340px;
	}
	.turnBox-enter {
		transform: rotateX(-90deg);
	}
	//* 进入状态
	.turnBox-enter-to {
		transform: rotateX(0deg);
		transform-origin: 50% 50% -340px;
	}

	//* 离开状态
	.turnBox-turnBack-leave {
	}
	.turnBox-turnBack-leave-to {
		transform: rotateX(-90deg);
		transform-origin: 50% 50% -340px;
	}
	.turnBox-turnBack-enter {
		transform: rotateX(90deg);
	}
	//* 进入状态
	.turnBox-turnBack-enter-to {
		transform: rotateX(0deg);
		transform-origin: 50% 50% -340px;
	}

}
</style>
