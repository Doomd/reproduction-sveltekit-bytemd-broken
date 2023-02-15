<script lang="ts">
	import { Editor, type BytemdPlugin } from 'bytemd';
	// import gfm from '@bytemd/plugin-gfm'

	let value: string = 'Something';
	const plugins: BytemdPlugin[] = [
		// gfm()
		// Add more plugins here
	];

	function handleChange(e) {
		value = e.detail.value;
	}
</script>

<div class="text-column">
	<h1>Bytemd Editor on Sveltekit 1.0+</h1>
	<p>
		<Editor bind:value {plugins} on:change={handleChange} />
	</p>
</div>
