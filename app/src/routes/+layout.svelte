<script lang="ts">
	import '../app.css';
	import Nav from '$lib/Nav.svelte';

	// pull layout data if you need it later
	const { data } = $props<{ data?: unknown }>();
</script>

<div class="layout">
	<Nav />

	<main>
		<slot />
	</main>
</div>
