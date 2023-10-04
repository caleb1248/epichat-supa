<script>
</script>

<nav class="top-navbar" style="height: 50px;">
	<span class="appname">Supa thing</span>
	<div>
		<a href="/login" style="margin-right: 1rem">Login</a>
		<a href="/signup" class="bluebg">Sign up</a>
	</div>
</nav>
<main>
	<h1 style="font-size: 4em; margin-top: 0; margin-bottom: 0.5em">Supa-thing</h1>
	<div class="rest">
		<p>A thingy that uses supabase</p>
		<div class="links">
			<a href="/signup" class="bluebg" style="width: 100%;">Start</a>
		</div>
	</div>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 3rem;
		flex: auto;
	}

	div.links {
		display: flex;
		justify-content: center;
		flex-direction: row;
		gap: 1rem;
	}

	a.bluebg {
		background-color: hsl(200, 100%, 50%);
		margin-top: 1rem;
		padding: 0.6rem;
		border-radius: 5px;
		transition: all 0.2s;
	}

	div.links > a {
		text-align: center;
	}

	a.bluebg:hover {
		background-color: hsl(200, 100%, 68%);
	}
</style>
