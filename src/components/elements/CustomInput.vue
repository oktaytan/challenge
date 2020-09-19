<template>
	<div class="custom_input" :class="{ 'with-icon': icon }">
		<svg v-if="icon" class="custom_input_icon" width="14" height="18">
			<path
				d="M14 17a1 1 0 01-2 0 5 5 0 00-10 0 1 1 0 01-2 0 7 7 0 0114 0zM7 2a2 2 0 11-2 2 2 2 0 012-2zm0 6a4 4 0 10-4-4 4 4 0 004 4z"
			/>
		</svg>
		<input
			type="text"
			:placeholder="placeholder"
			@input="$emit('change', $event.target.value)"
		/>
	</div>
</template>

<script>
export default {
	name: 'CustomInput',
	props: {
		icon: {
			type: Boolean,
		},
		placeholder: {
			type: String,
		},
	},
};
</script>
