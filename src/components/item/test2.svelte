<script>
    import { createEventDispatcher} from 'svelte'; 
    export let test; 
    let input = '';

    const dispatch = createEventDispatcher();

    function sayHello() {
        dispatch('message', {
            text : 'Hello'
        });
    }

    function handleCLick() { 
        alert('hahahhaa');
    }
</script>

<h2>{test}</h2>

<button on:click={sayHello}>
    Click to say hello
</button>
<button on:click|once={handleCLick}>
    Test2
</button>

<input bind:value={input} placeholder='enter your name'>
<p> Hello {input || 'stranger'}!</p>