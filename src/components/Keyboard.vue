<template>
	<div>
		<h2>Keyboard</h2>
		<Key
			v-for="morseSymbol in availableMorseSymbols"
			:key="morseSymbol"
			:morseSymbol="morseSymbol"
			@morse-symbol-pressed="morseSymbolPressedListener"
		/>
	</div>
</template>

<script>
import Key from './Key.vue';

export default {
	name: 'Keyboard',
	props: [ 'availableMorseSymbols' ],
	components: {
		Key
	},
	methods: {
		morseSymbolPressedListener( morseSymbol ) {
			this.$emit( 'morse-symbol-pressed', morseSymbol );
		}
	}
};
</script>

<style scoped lang="scss">
button {
	display: inline-block;
}
</style>
