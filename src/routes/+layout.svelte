<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<div class="h-screen w-full">
	<main class="mx-auto max-w-3xl flex justify-center items-center flex-col pt-20">
		{@render children()}
	</main>
</div>
