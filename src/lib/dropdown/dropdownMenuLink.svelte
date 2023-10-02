<script lang="ts">
	import { goto } from '$app/navigation';
	import { getContext } from 'svelte';

	export let href: string;

	const setIsOpen = (getContext('dropdown') as { setIsOpen: (value: boolean) => void }).setIsOpen!;
</script>

<div class="link-container">
	<button
		on:click={() => {
			setIsOpen(false);
			goto(href);
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
