<template>
	<div id="index">
		<web-header></web-header>
		<carousel-map type="turnBox"></carousel-map>
	</div>  
</template>

<script>
import webHeader from '@/components/webHeader'
import carouselMap from '@/components/carouselMap' //* 可选属性 type(过渡类型)：turnBox(翻转盒子), dalay(自动播放时间间隔): number
export default {
	components: { webHeader, carouselMap }
}
</script>
