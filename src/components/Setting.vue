<template>
	<div class="setting" :class="[orientation]">
		<span class="setting_title">{{ label }}</span>

		<template v-if="field === 'input'">
			<custom-input></custom-input>
		</template>

		<template v-if="field === 'dropdown'">
			<dropdown :optionData="data" @change="changeDrop"></dropdown>
		</template>

		<template v-if="field === 'button'">
			<custom-button type="outline" :text="text"></custom-button>
		</template>
	</div>
</template>

<script>
import CustomInput from './elements/CustomInput';
import DropDown from './elements/DropDown';
import CustomButton from './elements/CustomButton';

export default {
	name: 'Setting',
	components: {
		'custom-input': CustomInput,
		'custom-button': CustomButton,
		dropdown: DropDown,
	},
	props: {
		label: {
			type: String,
		},
		field: {
			type: String,
			required: true,
		},
		text: {
			type: String,
		},
		data: {
			type: Array,
		},
		orientation: {
			type: String,
			default: 'row',
		},
	},
	methods: {
		changeDrop(item) {
			console.log(item);
		},
	},
};
</script>
