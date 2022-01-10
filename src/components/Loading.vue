<template>
	<div :class="loadingObject">
		<slot />
	</div>
</template>

<script>
	export default {
		name: 'Loading',
		computed: {
			loadingObject() {
				return {
					loading: true,
					'loading-rounded': this.rounded,
					'loading-animated': this.animated
				};
			}
		},
		props: {
			rounded: {
				type: Boolean,
				default: true
			},
			animated: {
				type: Boolean,
				default: true
			}
		}
	};
</script>

<style lang="scss" scoped>
	@import '../scss/style.scss';
</style>
