<script>
	let count = 0;

	function incrementCount() { // Event handler
		count += 1;
	}
</script>

<button on:click={incrementCount}>  <!-- Bind click to event handler -->
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
