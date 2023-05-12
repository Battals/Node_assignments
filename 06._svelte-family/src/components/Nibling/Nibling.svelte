<script>
    export let nibling;
    export let onShowLove;
    export let piblingName;
</script>

<div class:is-girl={nibling.isGirl} 
    class:is-boy={!nibling.isGirl} 
    class={nibling.blackSheep || "not-a-black-sheep"} >
{#if nibling.isGirl}
    <p>Niece: {nibling.name}</p>
{:else}
    <p>Nephew: {nibling.name}</p>
{/if}
</div>
<button on:click={() => onShowLove(`Hey ${piblingName}. It's me ${nibling.name} and I love you.`)}>Show Love</button>


<!-- Task: A nibling should be allowed to ask a pibling for allowance 
    A nibling should have a certain amount of money
    When they ask for allowance all niblings should get 100 of whatever currency
-->

<style>
    .is-girl {
        border: 3px solid blue;
    }

    .is-boy {
        border: 3px solid pink;
    }

    .not-a-black-sheep {
        background-color: aliceblue;
        color: black;
    }

    .medium-black-sheep {
        background-color: burlywood;
    }

    .ultra-black-sheep {
        background-color: brown;
    }
</style>