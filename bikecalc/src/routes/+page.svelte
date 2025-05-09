<script>
	const pages = [
		{ name: 'Tire Pressure Calculator', path: '/tire_pressure' },
		{ name: 'Lorem', path: '' },
		{ name: 'Ipsum', path: '' }
	];
</script>

<div class="flex min-h-screen flex-col items-center justify-center bg-gray-100 p-4">
	<div class="grid grid-cols-1 gap-4 md:grid-cols-3">
		{#each pages as page}
			<a
				href={page.path}
				class="rounded-lg bg-slate-600 px-4 py-2 text-center text-lg text-white transition hover:bg-slate-800"
			>
				{page.name}
			</a>
		{/each}
	</div>
</div>
