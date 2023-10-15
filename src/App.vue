<template>
	<div>
		<h1>Hello, welcome!</h1>
		<h3>Here are many child components:</h3>
	</div>
<!-- Step 3 Use the component in the template -->
	<div>
		<!-- <SimpleMessage />
		<SimpleMessage /> -->
		<Counter :maxValue="30" :minValue="0"/>
		<Counter :maxValue="20" :minValue="5"/>
	</div>

</template>

<script>
//Step1: import the componet file
import SimpleMessage from './components/SimpleMessage.vue';
import Counter from './components/Counter.vue';

export default {
	// Step 2 register the component
	components: {
		SimpleMessage,
		Counter
	}
}
</script>
