<script>
export default {
	data() {
		return {
			message: "Hello!",
		}
	}
}
</script>

<template>
	<div>
		<h2>The message is:{{ message }}</h2>
	</div>
	<input type="text" v-model="message"/>
</template>

<style>
</style>
