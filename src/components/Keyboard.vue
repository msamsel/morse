<template>
	<div>
		<h2>Keyboard</h2>
		<div v-for="morseSymbol in availableMorseSymbols" :key="morseSymbol">
			<Key :morseSymbol="morseSymbol" @morse-symbol-pressed="keyPressedListener"/>
		</div>
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
		keyPressedListener( morseSymbol ) {
			window.console.log( morseSymbol );
		}
	}
};
</script>

<style scoped lang="scss">
button {
	display: inline-block;

}
</style>
