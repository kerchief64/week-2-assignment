<script>
	import Thing from './Thing.svelte';

    let things = [
		{ id: 1, color: 'darkblue' },
		{ id: 2, color: 'indigo' },
		{ id: 3, color: 'deeppink' },
		{ id: 4, color: 'salmon' },
		{ id: 5, color: 'gold' }
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<button on:click={handleClick}>
	Remove first thing
</button>

<div style="display: grid; grid-template-columns: 1fr 1fr; grid-gap: 1em">
	<div>
		<h2>Color Block Sets</h2>
        <!-- 
            Test the "Remove first thing" button, take a mental note of the (bugged) behavior.
            Set a custom key on this each block so that the colors stay in sync when they are deleted

            Note: You may also need to add missing information to the "things" variable in the <script> above to make this work.
         -->
		{#each things as thing (thing.id)}
			<Thing current={thing.color}/>
		{/each}
	</div>
</div>
