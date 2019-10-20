<template>
	<div>
		<h2>Preview</h2>
		<div class="preview-wrapper">
			<PreviewItem v-for="(item, index) in previewItems" :key="index" :item="item" />
		</div>
	</div>
</template>

<script>
import PreviewItem from './PreviewItem.vue';

export default {
	name: 'Preview',
	props: [ 'previewItems' ],
	components: {
		PreviewItem
	}
};
</script>

<style scoped>
	.preview-wrapper {
		height: 2em;
		border: 1px solid var( --main-dark-color );
		margin: 0.2em;
	}
</style>
