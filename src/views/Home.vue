<template>
	<div>
		<Preview :previewItems="previewItems"/>
		<Keyboard
			:availableMorseSymbols="availableMorseSymbols"
			@morse-symbol-pressed="morseSymbolPressedListener"
		/>
	</div>
</template>

<script>
import Keyboard from '../components/Keyboard.vue';
import Preview from '../components/Preview.vue';
import { getMorseSymbols } from '../utils/utils';

export default {
	name: 'Home',
	components: {
		Keyboard,
		Preview
	},
	data() {
		return {
			availableMorseSymbols: getMorseSymbols(),
			previewItems: []
		};
	},
	methods: {
		morseSymbolPressedListener( morseSymbol ) {
			this.previewItems.push( morseSymbol );
			window.console.log( morseSymbol );
		}
	}
};
</script>

<style>

</style>
