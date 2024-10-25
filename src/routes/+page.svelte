<script>
	import Svg from '../lib/assets/circle.svg';
	let colors = $state(['#BBFF00', '#06F586', '#ff3e00', '#8D462E', '#FF0037']);

	let fillings = $state(0);

	$effect(() => {
		console.log(fillings);
	});
</script>

<div>
	<div class="flex gap-2 mb-4">
		{#each colors as color, index}
			<div class="flex flex-col gap-2">
				<button
					onclick={() => (fillings = index)}
					style:background={colors[index]}
					class="w-24 h-24 mb-3 rounded-full"
				>
					{#if index === fillings}
						<img src={Svg} alt={index.toString()} />
					{/if}
				</button>
				<span>
					<code>
						{colors[index]}
					</code>
				</span>
			</div>
		{/each}
	</div>
	<input bind:value={colors[fillings]} type="color" name="color" />
</div>
