<script>
	let pieces = 1;
	let fruits = ['Kiwi'];

	let menu = [
		'Kiwi',
		'Mango',
		'Pear'
	];

	function join(fruits) {
		if (fruits.length === 1) return fruits[0];
		return `${fruits.slice(0, -1).join(', ')} and ${fruits[fruits.length - 1]}`;
	}
</script>

<h1>Example 2</h1>

<h2>Quantity</h2>

<label>
	<input type=radio bind:group={pieces} value={1}>
	One piece
</label>

<label>
	<input type=radio bind:group={pieces} value={2}>
	Two pieces
</label>

<label>
	<input type=radio bind:group={pieces} value={3}>
	Three pieces
</label>

<h2>Fruits</h2>
{#each menu as fruit}
	<label>
		<input type=checkbox bind:group={fruits} value={fruit}>
		{fruit}
	</label>
{/each}

{#if fruits.length === 0}
	<p>Please select at least one fruit</p>
{:else if fruits.length > pieces}
	<p>Can't order more fruits than pieces!</p>
{:else}
	<p>
		You ordered {pieces} {pieces === 1 ? 'piece' : 'pieces'}
		of {join(fruits)}
	</p>
{/if}

<style>
	h1 {
	  color: aqua;
	  text-transform: uppercase;
	  font-size: 4rem;
	  font-weight: 100;
	}
  </style>