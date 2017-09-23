<template>
	<div id="index">
		<web-header></web-header>
		<carousel-map></carousel-map>
	</div>  
</template>

<script>
import webHeader from '@/components/webHeader'
import carouselMap from '@/components/carouselMap'
export default {
	components: { webHeader, carouselMap }
}
</script>
