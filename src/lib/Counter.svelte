<script>
	let count = 0;
  $: doubled = count * 2  // Re-run this code whenever any of the referenced values change

	function incrementCount() { // Event handler
		count += 1;
	}
</script>

<button on:click={incrementCount}>  <!-- Bind click to event handler -->
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
<p>
  {count} doubled is {doubled}
</p>
