<template>
	<code>{{ item }}</code>
</template>

<script>
export default {
	name: 'PreviewItem',
	props: [ 'item' ]
};
</script>

<style scoped>
	code {
		margin: 0 0.3em;
	}
</style>
