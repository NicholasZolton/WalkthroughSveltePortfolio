<script lang='ts'>
	var sorting_array = Array.from({length: 50}, () => Math.floor(Math.random() * 100));
	var ranAlready = false;

	async function bubbleSort() {
		if (ranAlready) {
			sorting_array = Array.from({length: 50}, () => Math.floor(Math.random() * 99) + 1);	
		}
		ranAlready = true;

		var moved = true;
		while (moved) {
			moved = false;
			for(var i = 0; i < sorting_array.length - 1; i++) {
				if(sorting_array[i] > sorting_array[i + 1]) {
					var temp = sorting_array[i];
					sorting_array[i] = sorting_array[i+1];
					sorting_array[i+1] = temp;
					await new Promise(r => setTimeout(r, 100));
					moved = true;
				}
			}
		}
	}
</script>

<main>
	<h1>Here's my simple Bubble Sort!</h1>
	<div id="graph">
		{#each sorting_array as num, index}
			{#if index != sorting_array.length - 1}
				<div class="graph-bar" style="width: 1%; height: {num}%;"/>
				<div class="graph-divider" style="width: 0.5%;"/>
			{:else}
				<div class="graph-bar" style="width: 1%; height: {num}%;"/>
			{/if}
		{/each}
	</div>
	<button id="start-button" on:click={bubbleSort}>
		Click here to begin!
	</button>
</main>

<style>

	main {
		padding: 2%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	#start-button {
		margin-top: 1%;
		height: 80%;
		width: 80%;
	}

	.graph-bar {
		transition: 0.5s;
		background-color: aqua;
	}

	#graph {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: flex-end;
		height: 60vh;
		width: 80vw;
	}

</style>