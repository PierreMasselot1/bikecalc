<script>
	import { onMount } from 'svelte';
	import Chart from 'chart.js/auto';

	let chart;

	onMount(() => {
		const ctx = document.getElementById('myChart').getContext('2d');
		chart = new Chart(ctx, {
			type: 'line',
			data: {
				labels: ['20mm', '25mm', '30mm', '35mm'],
				datasets: [
					{
						label: 'Ideal Pressure (psi)',
						data: [110, 100, 90, 80],
						borderColor: 'rgb(75, 192, 192)',
						tension: 0.1
					}
				]
			},
			options: {
				responsive: true,
				scales: {
					x: {
						title: {
							display: true,
							text: 'Tire Width (mm)'
						}
					},
					y: {
						title: {
							display: true,
							text: 'Pressure (psi)'
						},
						beginAtZero: true
					}
				}
			}
		});
	});
	const bike_types = [
		{ n: 'TT', c: 'bg-blue-500' },
		{ n: 'Road', c: 'bg-yellow-500' },
		{ n: 'Gravel', c: 'bg-neutral-500' },
		{ n: 'MTB', c: 'bg-green-500' }
	];
</script>

<div class="flex items-center">
	<div class="flex self-start">
		{#each bike_types as bike}
			<button class="{bike.c} m-2 rounded-md px-4 py-2">
				{bike.n}
			</button>
		{/each}
	</div>
	<canvas id="myChart" class="w-600" height="400"></canvas>
</div>
