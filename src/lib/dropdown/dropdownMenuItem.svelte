<script lang="ts">
	import { createEventDispatcher, getContext } from 'svelte';

	const setIsOpen = (getContext('dropdown') as { setIsOpen: (value: boolean) => void }).setIsOpen!;
	if (!setIsOpen) console.error('Dropdown component not parent');

	const dispatcher = createEventDispatcher();
</script>

<div class="link-container">
	<button
		on:click={() => {
			setIsOpen(false);
			dispatcher('click');
		}}
	>
		<slot />
	</button>
</div>

<style lang="scss">
	div.link-container {
		background-color: #555;
		padding: 1rem;
		display: flex;
		button {
			font: inherit;
			color: #222;
			background: inherit;
			border: none;
			cursor: pointer;
			&:hover {
				color: black;
			}
		}
	}
</style>
