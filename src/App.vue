<template>
	<div id="app">
		<router-view></router-view>
	</div>
</template>

<script>
export default {
	name: 'app'
}
</script>

<style lang='scss'>
//* reset styel
html, body {
	margin: 0;
	padding: 0;
}
h1, h2, h3, h4, h5, h6, p {
	margin: 0;
}
ul {
	margin: 0;
	padding: 0;
	list-style-type: none;
}
//* costom attribute
.clearfix {
	&::before, &::after {
		content: "";
		display: block;
		clear: both;
	}
}
//* iconfont symbol格式通用代码
.icon {
		width: 1em; height: 1em;
		vertical-align: -0.15em;
		fill: currentColor;
		overflow: hidden;
}
</style>