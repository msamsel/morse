<template>
	<div>
		<h2>Keyboard</h2>
		<div v-for="(value, key, index) in keyButtons" :key="index">
			<Key :letter="key" :code="value" />
		</div>
	</div>
</template>

<script>
import Key from './Key.vue';

export default {
	name: 'Keyboard',
	props: [ 'keyButtons' ],
	components: {
		Key
	}
};
</script>

<style>

</style>
