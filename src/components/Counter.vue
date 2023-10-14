<script>

export default {
	data() {
		return {
			count : 0,
		}
	},
	methods: {
		decrease() {
			if (this.count > 0) this.count--;
		}
	}
}

</script>

<template>
	<div>
		<h3>The count is: {{ count }}</h3>
		<button @click="count++">+1</button>
		<button @click="decrease" :disabled="count === 0">-1</button>
	</div>

</template>

<style>
</style>

