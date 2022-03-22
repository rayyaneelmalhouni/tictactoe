<script>
    import Square from "./Square.svelte";
    let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    export let squares;
    console.log(squares)
    
</script>
<style>
   div {
        margin: 0 auto;
        width: 300px;
        height: 300px;
        border: 2px solid blue;
        margin-top: 20px;
        display: flex;
        flex-wrap: wrap;
   }
</style>
<div>
    {#each squares as look ,i}
	<Square {i} {look} on:message />
	{/each}
</div>