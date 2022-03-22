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
       margin: 0 auto;
   }
   .icon span {
     height: 60px;
     border: 4px solid pink;
     border-radius: 4px;
   }
   .left {
        transform: rotate(50deg);
   }
   .right {
        transform: rotate(-50deg);
   }
   .circle {
       border: 4px solid pink;
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


<div class="square">
    <!-- <div class="icon">
        <span class="left"></span>
        <span class="right"></span>
    </div>  -->
 <div class="circle-container">
        <div class="circle">

        </div>      
    </div>
        
    

</div>