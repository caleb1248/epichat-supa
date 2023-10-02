<script lang="ts">
	import { setContext } from 'svelte';

	let isOpen = false;

	function setIsOpen(open: boolean) {
		isOpen = open;
	}

	setContext('dropdown', { setIsOpen });
</script>

<div class="dropdown" on:blur={() => setIsOpen(false)}>
	<slot name="dropdownBtn" {setIsOpen} />
	<div class="dropdown-content" style="display: {isOpen ? 'block' : 'none'}">
		<slot {setIsOpen} />
	</div>
</div>

<style>
	.dropdown {
		position: relative;
		display: inline-block;
	}

	.dropdown-content {
		position: absolute;
		top: var(--dropdown-top);
		right: 10px;
		white-space: var(--white-space);
		box-shadow: 0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
		z-index: 1;
	}
</style>
