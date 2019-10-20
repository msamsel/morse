<template>
	<Keyboard :availableMorseSymbols="availableMorseSymbols" />
</template>

<script>
import Keyboard from '../components/Keyboard.vue';
import { getMorseSymbols } from '../utils/utils';

export default {
	name: 'Home',
	components: {
		Keyboard
	},
	data() {
		return {
			availableMorseSymbols: getMorseSymbols()
		};
	}
};
</script>

<style>

</style>
