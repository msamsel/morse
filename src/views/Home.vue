<template>
	<Keyboard :keyButtons="morseCodesMap" />
</template>

<script>
import Keyboard from '../components/Keyboard.vue';
import { morseCodes } from '../utils/utils';

export default {
	name: 'Home',
	components: {
		Keyboard
	},
	data() {
		return {
			morseCodesMap: morseCodes
		};
	}
};
</script>

<style>

</style>
