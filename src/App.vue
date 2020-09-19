<template>
	<div id="app">
		<CallView msg="Welcome to Your Vue.js App" />
	</div>
</template>

<script>
import CallView from './components/CallView.vue';

export default {
	name: 'App',
	components: {
		CallView,
	},
};
</script>

<style lang="scss">
@import './scss/main.scss';
</style>
