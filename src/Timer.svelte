
<script>

import ProgressBar from "./ProgressBar.svelte";



let count = 0 ; 
let reverse =  20; 
let isRunning = false ; 
$:progress  = count * 5 +"%";   // counts right side on the spot (makes QS pointless, Input into Progress bar / )
function timer () {
let myVar = setInterval(() => {
    isRunning = true;
    count +=1 ;
    reverse -=1;
    if (count === 20 ){
        clearInterval(myVar);
        isRunning = false ; 
        count = 0 ;
        reverse = 20 ; 
    }
}, 1000);}


</script>

<style>

h2{
    

    
    margin:0}
    
    .start{


        background-color: rgb(92, 43, 43);
        width:100%;
        margin: .2rem 0 ;
    }

    .start[disabled] {

        background-color: grey;
        cursor: not-allowed;
    }
    
    
    </style>


<div bp = "grid">

<h2 bp = "offset-5@md 4@md 12@sm">

Seconds Left: {reverse} 
</h2>


</div>
<ProgressBar {progress} />
<div bp = "grid">
<button disabled = {isRunning} on:click= {timer} bp = "offset-5@md 4@md 12@sm" class="start">Start</button>
</div>