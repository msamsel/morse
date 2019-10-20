<template>
	<button @click="$emit( 'morse-symbol-pressed', morseSymbol )">{{ morseSymbol }}</button>
</template>

<script>
export default {
	name: 'Key',
	props: [ 'morseSymbol' ]
};
</script>

<style>

</style>
