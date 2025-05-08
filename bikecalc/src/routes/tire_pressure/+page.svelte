<script>
	const bike_types = [
		{ n: 'TT', c: 'bg-blue-500' },
		{ n: 'Road', c: 'bg-yellow-500' },
		{ n: 'Gravel', c: 'bg-neutral-500' },
		{ n: 'MTB', c: 'bg-green-500' }
	];
</script>

<div class="flex items-center">
	{#each bike_types as bike}
		<button class="{bike.c} m-2 rounded-md px-4 py-2">
			{bike.n}
		</button>
	{/each}
</div>
