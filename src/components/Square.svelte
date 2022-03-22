<script>
    import { createEventDispatcher } from "svelte";
    export let i;
    export let look;
    const dispatch = createEventDispatcher();
    function click() {
        dispatch("message", {
            text: i + 1
        })
    }
    

</script>

<style>
   .square {
      width: 98.6px;
      height: 100px;
      border: 2px solid blue;
      
   }
   .icon {
       display: flex;
       justify-content: center;
       height: 100%;
       width: 100%;
       align-items: center;
       padding: 20px;
   }
   .icon span {
     height: 100px;
     border: 4px solid pink;
     border-radius: 4px;
   }
   .left {
        transform: rotate(45deg);
   }
   .right {
        transform: rotate(-45deg);
   }
   .circle {
       border: 6px solid pink;
       width: 80px;
       height: 80px;
       border-radius: 50%;
   }
   .circle-container {
       height: 100%;
    display: flex;
       justify-content: space-around;   
       align-items: center;
   }
</style>


<div class="square" on:click={click}>
    {#if look === "X"}
    <div class="icon">
        <span class="left"></span>
        <span class="right"></span>
    </div> 
    {:else if look === "O"}
    <div class="circle-container">
        <div class="circle">

        </div>      
    </div>
    {/if }
        
    

</div>