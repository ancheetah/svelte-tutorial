<script>
	let count = 0;
  $: doubled = count * 2  // Declare a reactive value
                          // Re-run this code whenever any of the 
                          // referenced values change

  $: if (count >= 10) { // Declare reactive statements
		alert('count is dangerously high!');
		count = 9;
		console.log('the count is ' + count); // Can also declare statements 
                                          // outside of "if" with {}
	}

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
