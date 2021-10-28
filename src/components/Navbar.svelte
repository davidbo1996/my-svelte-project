<script>
   

    let navbar_items = [
        {id : 1 , name: "Projets"},
        {id : 2, name: "Contact"},
        {id : 3, name:"More"}
    ]; 
	
</script>
<h1>Test</h1>
{#each navbar_items as { id, name }}
    <li>
        {id} : {name}
    </li>
{/each}