<script>
	let coordinates = { x: 0, y: 0 };

	function mousePosition(event) {
		coordinates.x = event.clientX;
		coordinates.y = event.clientY;
	}
</script>

<h1>Example 3</h1>
<div on:mousemove={mousePosition}>
	The mouse position = {coordinates.x} x {coordinates.y}
</div>

<style>
    h1 {
	  color: aqua;
	  text-transform: uppercase;
	  font-size: 4rem;
	  font-weight: 100;
	}
	div {
      background-color: beige;
      width: 100%;
      height: 5rem; 
    }
</style>