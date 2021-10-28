<script>
    import Test2 from './item/test2.svelte';
    let m = { x: 0, y: 0 };

function handleMousemove(event) {
    m.x = event.clientX;
    m.y = event.clientY;
}

function handleMessage(event) {
    alert(event.detail.text);
}
</script>

<div on:mousemove={handleMousemove}>
	The mouse position is {m.x} x {m.y}
    <Test2 test = {"Henri"} on:message={handleMessage}/>

</div>



<style>
	div { width: 100%; height: 100%; }
</style>