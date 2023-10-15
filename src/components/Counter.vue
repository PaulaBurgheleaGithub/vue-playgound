<script>

export default {
	props: {
		maxValue: {
			default: 10
		},
		minValue: {
			default: 0
		}
	},
	data() {
		return {
			count : 0
		}
	},
	methods: {
		decrease() {
			if (this.count > this.minValue) this.count--;
		},
		increase() {
			if (this.count < this.maxValue) this.count++;
		}
	}
}

</script>

<template>
	<div>
		<h3>Count up to {{ maxValue }} and decrease up to {{ minValue }}: 
			<span :class="{ 'text-danger': count<= minValue , 'text-success': count > minValue}">{{ count }}</span>
		</h3>
		<div class="btn-group">
			<button class="btn btn-outline-dark" @click="increase" :disabled="count === maxValue">+1</button>
			<button class="btn btn-outline-dark" @click="decrease" :disabled="count === minValue">-1</button>
		</div>
	</div>

</template>

<style>
</style>

