<template>
	<div id="carouselMap">
		<div class="imgList">
			<transition name="fade">
				<img :src="img" v-for="(img, imgIndex) in imgs" :key="imgIndex" v-if="active === imgIndex">
				<!-- <img :src="imgs[active]"> -->
			</transition>
		</div>
		<div class="handel">
			<div class="point" v-if="isPoint">
				<div 
				:class="pointIndex === active ? 'round active' : 'round'" 
				v-for="(point, pointIndex) in imgs" 
				:key="pointIndex"
				@click="active = pointIndex"></div>
			</div>
			<div class="handler">
				<div class="left" @click="active--">
					<svg class="icon" aria-hidden="true">
						<use xlink:href="#icon-lt"></use>
					</svg>
				</div>
				<div class="right" @click="active++">
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
			]
		}
	},
	watch: {
		active() {
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
	.fade-enter-active, .fade-leave-active {
		transition: opacity .5s
	}
	.fade-enter, .fade-leave-to/* .fade-leave-active in below version 2.1.8 */ {
		opacity: 0;
	}
}
</style>
