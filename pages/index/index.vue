<template>
	<view>
		<web-view ref="webview" :src="src"></web-view>
	</view>
</template>

<script>
	// const url = "http://112.111.13.209:57358/msr-app"
	// const url = "http://172.16.6.224:53100/mlr-app";
	const url = "https://172.16.6.224:53101/mlr-app";
	export default {
		onLoad() {
			// try{
			// 	const windowInfo = uni.getWindowInfo();
			// 	const barHeight = windowInfo.statusBarHeight;
			// 	const webviews = this.$scope.$getAppWebview();
			// 	setTimeout(() => {
			// 	  const webview = webviews.children()[0];
			// 	  webview.evalJS(`window.setSaftBarHeight(${barHeight})`);
			// 	}, 1000);
			// }catch(e){
			// 	//TODO handle the exception
			// }

		},
		computed: {
			src() {
				return `${url}`;
			},
		},
		// onBackPress(e) {
		// 	this.webview.evalJS('window.back()')
		// 	return true
		// }
		onBackPress(e) {
			this.$scope
				.$getAppWebview()
				.children()[0]
				.back();
				console.log("????")
			return true;
		}

	};
</script>

<style></style>