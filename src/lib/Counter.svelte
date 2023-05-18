<script>
  let count = 0

  const increment = () => {
    count += 1
  }

  const decrement = () => {
    count -= 1
  }
</script>

<h1>Simple Counter!</h1>
<p>{count}</p>
<button on:click={increment}>+</button>
<button on:click={decrement}>-</button>

<style>
  h1 {
    color: aqua;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
  }
  
  p {
    font-size: 3em;
  }
</style>