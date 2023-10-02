<script lang="ts">
	import { getContext } from 'svelte';

	const setIsOpen = (getContext('dropdown') as { setIsOpen: (value: boolean) => void }).setIsOpen!;
	if (!setIsOpen) console.error('Dropdown component not parent');
</script>

<button class="dropdown-button" on:click={() => setIsOpen(true)}><slot /></button>
