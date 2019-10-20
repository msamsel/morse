<template>
	<Keyboard
		:availableMorseSymbols="availableMorseSymbols"
		@morse-symbol-pressed="morseSymbolPressedListener"
	/>
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
	},
	methods: {
		morseSymbolPressedListener( morseSymbol ) {
			window.console.log( morseSymbol );
		}
	}
};
</script>

<style>

</style>
