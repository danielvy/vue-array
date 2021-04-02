<template>
	<h1>Vue array type</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

interface MyArray extends Array<number> {};

export default defineComponent({
  name: 'App',
	data() {
		return {
			array: [] as MyArray
		}
	},

	mounted() {
		const x: Array<number> = this.array;
		const y: MyArray = this.array;
		console.log(x, y);
	}

});
</script>


