<script lang="ts">
	export let data;

	let email: string;
	let password: string;
</script>

<main>
	<h1>Login</h1>
	<input bind:value={email} />
	<input type="password" bind:value={password} />
</main>

<style>
	main {
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
