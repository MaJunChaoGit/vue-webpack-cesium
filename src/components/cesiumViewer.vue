<template>
	<div id="cesiumContainer"></div>
</template>

<script>
import Viewer from "cesium/Source/Widgets/Viewer/Viewer";
import buildModuleUrl from "cesium/Source/Core/buildModuleUrl"
import "cesium/Source/Widgets/widgets.css";


export default{
	name:"cesiumContainer",
	mounted:function () {
		buildModuleUrl.setBaseUrl('../static/cesium/')
		this.viewer = new Viewer('cesiumContainer');
	},
	data () {
		return {
			'viewer' : {}
		}
	}
}
</script>

<style scoped>

</style>