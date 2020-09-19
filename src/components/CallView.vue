<template>
	<section class="card">
		<call-details></call-details>

		<video-container></video-container>

		<custom-input :icon="true" placeholder="Username"></custom-input>

		<!-- Settings - START -->
		<div class="settings">
			<setting
				v-for="setting in settings"
				:key="setting.id"
				:label="setting.label"
				:field="setting.field"
				:text="setting.text"
				:data="setting.data"
				orientation="row"
			></setting>
		</div>
		<!-- Settings - END -->

		<custom-button type="primary" text="Join Call"></custom-button>
	</section>
</template>

<script>
import CallDetails from './CallDetails';
import Video from './Video';
import Setting from './Setting';
import CustomInput from './elements/CustomInput';
import CustomButton from './elements/CustomButton';

export default {
	name: 'CallView',
	components: {
		'call-details': CallDetails,
		'video-container': Video,
		'custom-input': CustomInput,
		'custom-button': CustomButton,
		setting: Setting,
	},
	data() {
		return {
			settings: [
				{
					id: 1,
					label: 'Camera',
					field: 'dropdown',
					text: null,
					data: [
						{ op_id: 1, option: 'Facetime HD Camera' },
						{ op_id: 2, option: 'FullHD Camera' },
						{ op_id: 3, option: 'Device Webcam' },
					],
				},
				{
					id: 2,
					label: 'Speaker',
					field: 'dropdown',
					text: null,
					data: [
						{ op_id: 1, option: 'Built-in Output (Headphone)' },
						{ op_id: 2, option: 'Lorem ipsum' },
						{ op_id: 3, option: 'Lorem ipsum' },
					],
				},
				{
					id: 3,
					label: 'Microphone',
					field: 'dropdown',
					text: null,
					data: [
						{ op_id: 1, option: 'Built-in Microphone (Entire)' },
						{ op_id: 2, option: 'Lorem ipsum' },
						{ op_id: 3, option: 'Lorem ipsum' },
					],
				},
				{
					id: 4,
					label: 'Sound Test',
					field: 'button',
					text: 'Play Sound',
					data: null,
				},
			],
		};
	},
};
</script>
