<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
        // Updating arrays
		// numbers.push(numbers.length + 1);
        // numbers = numbers
        // OR
        // numbers = [...numbers, numbers.length + 1]
        // OR
        numbers[numbers.length] = numbers.length + 1;   // Assignment to property
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>

<!-- 
    Indirect assignments like:

    const foo = obj.foo;
    foo.bar = 'baz';

    won't trigger rectivity on obj.foor.bar unless you follow with:

    obj = obj
 -->