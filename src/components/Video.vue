<template>
	<div class="video">
		<video-preview></video-preview>
		<video-controls></video-controls>
	</div>
</template>

<script>
import VideoPreview from './VideoPreview';
import VideoControls from './VideoControls';

export default {
	name: 'CallView',
	components: {
		'video-preview': VideoPreview,
		'video-controls': VideoControls,
	},
};
</script>
