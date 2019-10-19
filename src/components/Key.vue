<template>
	<button>{{ buttonString }}</button>
</template>

<script>
export default {
	name: 'Key',
	props: [ 'letter', 'code' ],
	computed: {
		buttonString() {
			return this.letter + ' ' + this.code;
		}
	}
};
</script>

<style>

</style>
