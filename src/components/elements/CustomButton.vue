<template>
	<button
		class="btn"
		:class="{
			'btn-outline': type === 'outline',
			'btn-primary': type === 'primary',
			'btn-danger': type === 'danger',
			'btn-default': type === 'default',
		}"
		@click="$emit('click')"
		>{{ text }}</button
	>
</template>

<script>
export default {
	name: 'CustomButton',
	props: {
		text: {
			type: String,
			required: true,
		},
		type: {
			type: String,
		},
	},
};
</script>
