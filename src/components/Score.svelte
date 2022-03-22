<script>
      import { createEventDispatcher } from "svelte";
    export let turn;
    export let winner;
    const dispatch = createEventDispatcher();
    function retry() {
        dispatch("retry", {})
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Red+Hat+Mono:wght@500&display=swap');
    h1 {
        text-align: center;
        font-size: 1.6em;
        font-family: 'Red Hat Mono', monospace;
    }
    .winner {
        color: pink;
    }
    .turn {
        color: violet;
    }
    .retry-btn {
        text-align: center;
        padding: 10px 20px;
        border-radius: 15px;
        background-color: red;
        border: none;
        color: #F9F9F9;
    }
    .retry-btn:hover {
        background-color: rgb(255, 212, 219);
    }
    .btn-container {
        display: flex;
        justify-content: center;
        margin: 20px;
    }
</style>

{#if !winner}<h1 class="turn">{#if turn}You're turn{:else}Dealer's turn{/if}</h1>
{:else }<h1 class="winner">{#if winner === "X"}You Won{:else if winner === "O"}You lose {:else} Tie{/if}</h1>
<div class="btn-container"><button class="retry-btn" on:click={retry}>Retry</button></div>
{/if}

