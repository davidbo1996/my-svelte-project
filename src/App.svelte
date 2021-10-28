<script>
	import Test from './components/Test.svelte';
	import Navbar from './components/Navbar.svelte';
	import EventMouse from './components/EventMouse.svelte';
	import AddEvent from './components/AddEvent.svelte';

	export let url_api ="https://ptahir785a.execute-api.eu-west-1.amazonaws.com/calendar_event";

	async function createEventMorning() {
		
		const res = await fetch(url_api, {
			method : 'POST', 
			headers: {
            "Access-Control-Allow-Headers" : "Content-Type",
            "Access-Control-Allow-Origin": "localhost",
            "Access-Control-Allow-Methods": "OPTIONS,POST,GET"
        	},
			body: JSON.stringify({
				"user_id": "user_200mN2XCeyYy4ZMwoPpVGGuz0Vh",
    			"resource_id": "res_203C1oGB43f8atkvXBzDIPhHI0d",
    			"created_date": "2021-10-26T04:26:15.261Z",
    			"start_time": "2021-12-19T14:00",
    			"end_time": "2021-12-19T18:00",
    			"is_full_day_event": false,
    			"is_recurring": 0,
    			"am": true
			})
		}).then((resultat)=>{
			console.log(resultat)
		}).catch(err=>{
			console.log(err)
		}).finally(()=>{

		});
	
	}
	
</script>


<button on:click={createEventMorning}>
	test POST 
</button>

<!-- <Test answer={42} />
<Navbar />
<EventMouse /> -->



    
