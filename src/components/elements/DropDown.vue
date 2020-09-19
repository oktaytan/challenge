<template>
	<div class="dropdown" :class="{ show: shown }">
		<svg class="dropdown_icon" width="9" height="7">
			<path
				d="M4.501 6.75a1.276 1.276 0 01-.99-.482L.351 2.445a1.559 1.559 0 01-.2-1.658A1.329 1.329 0 011.341 0h6.32a1.329 1.329 0 011.19.787 1.576 1.576 0 01-.19 1.657l-3.17 3.824a1.276 1.276 0 01-.99.482z"
			/>
		</svg>
		<div class="selected_item" ref="dropdown" @click="listClicked">
			<p>{{ selected }}</p>
		</div>

		<ul class="dropdown_list">
			<li
				v-for="item in optionData"
				:key="item.op_id"
				class="dropdown_list_item"
				@click="selectOption(item)"
			>
				<p>{{ item.option }}</p>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: 'DropDown',
	props: {
		optionData: {
			type: Array,
			required: true,
		},
	},
	data() {
		return {
			selected: '',
			shown: false,
		};
	},
	created() {
		this.selected = this.optionData[0].option;
	},
	methods: {
		documentClick(e) {
			try {
				let el = this.$refs.dropdown;
				let target = e.target;
				if (el !== target && !el.contains(target)) {
					el.parentElement.classList.remove('show');
				} else {
					el.parentElement.classList.add('show');
				}
			} catch (error) {}
		},
		selectOption(item) {
			this.selected = item.option;
			let option = {
				value: item.op_id,
				option: item.option,
			};
			this.$emit('change', option);
			let el = this.$refs.dropdown;
			el.parentElement.classList.remove('show');
		},
		listClicked() {
			this.shown = !this.shown;
		},
	},
	beforeMount() {
		document.addEventListener('click', this.documentClick);
	},
	beforeDestroy() {
		document.removeEventListener('click', this.documentClick);
	},
};
</script>
