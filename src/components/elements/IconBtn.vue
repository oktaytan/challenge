<template>
	<button class="icon_btn" v-html="icon" @click="$emit('click')"></button>
</template>

<script>
export default {
	name: 'IconBtn',
	props: ['icon'],
};
</script>
