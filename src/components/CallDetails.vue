<template>
	<div class="call_details">
		<div class="call_title">
			<a href="#" class="default_link">Call with</a>
			<h1 class="call_title_name">Niloya Kayıkçı</h1>
		</div>

		<date-time></date-time>
	</div>
</template>

<script>
import DateAndTime from './DateAndTime';

export default {
	name: 'CallDetails',
	components: {
		'date-time': DateAndTime,
	},
};
</script>
