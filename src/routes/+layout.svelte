<script lang="ts">
	import '../app.css';
	const year = new Date().getFullYear();
</script>

<page>
	<header>
		<a href="/"><logo>SvelteKit Site</logo></a>
		<nav>
			<!-- <a href="/">Home</a> -->
			<a href="/editor">ByteMD Editor</a>
			<a href="/viewer">ByteMD Viewer</a>
		</nav>
	</header>
	<main>
		<div class="note">
			NOTE: Clicking on the upper right nav links will fail to load the ByteMD components. But if
			you refresh the respective pages (or directly load the /viewer or /editer urls) into the
			browser with the link in the address bar, the Bytemd components will render (but there are
			still tons of errors in the console, and the Editor fails to edit.).
		</div>
		<slot />
	</main>
	<footer>Sveltekit Site &copy;{year}</footer>
</page>

<style>
	page {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 1rem;
	}
	header,
	footer {
		background: #ccc;
		padding: 1rem;
		display: flex;
	}
	header {
		justify-content: space-between;
	}
	nav {
		display: flex;
		gap: 1rem;
	}
	main {
		flex: auto;
		padding: 1rem;
	}
	.note {
		background: rgb(189, 255, 189);
		border-radius: 0.5rem;
		padding: 0.5rem;
	}
	footer {
		justify-content: center;
	}
</style>
