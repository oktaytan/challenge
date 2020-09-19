<template>
	<div class="wrapper text-center">
		<div class="date_and_time">
			<div class="date">
				<svg
					class="icon icon-primary"
					xmlns="http://www.w3.org/2000/svg"
					width="13.5"
					height="15"
				>
					<path
						d="M12 6.75H1.5v-3A.753.753 0 012.25 3H3v.75a.75.75 0 001.5 0V3H9v.75a.75.75 0 001.5 0V3h.75a.753.753 0 01.75.75zm-2.25 4.5h-3a.75.75 0 010-1.5h3a.75.75 0 010 1.5zm-6 0a.75.75 0 11.75-.75.753.753 0 01-.75.75zm7.5-9.75h-.75V.75a.75.75 0 00-1.5 0v.75H4.5V.75a.75.75 0 00-1.5 0v.75h-.75A2.253 2.253 0 000 3.75v9A2.253 2.253 0 002.25 15h9a2.253 2.253 0 002.25-2.25v-9a2.253 2.253 0 00-2.25-2.25z"
					/>
				</svg>
				<span>7 Oct, Weds</span>
			</div>
			<div class="time">
				<svg
					class="icon icon-primary"
					xmlns="http://www.w3.org/2000/svg"
					width="15"
					height="15"
				>
					<path
						d="M10.5 8.25h-3a.752.752 0 01-.75-.75v-3a.75.75 0 011.5 0v2.25h2.25a.75.75 0 010 1.5zM7.5 0A7.5 7.5 0 1015 7.5 7.506 7.506 0 007.5 0z"
					/>
				</svg>
				<span>10:15AM - 10:30AM</span>
			</div>
		</div>

		<span class="timezone">Timezone: Europe/Amsterdam</span>
	</div>
</template>

<script>
export default {
	name: 'DateAndTime',
};
</script>
