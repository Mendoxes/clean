

<script>
export let progress = 0 ;
  

    </script>



<style>

.progress-container{
border: solid white 1px ;

margin: 20px 0 ;

}



.progress-bar {

    height: 30px ;
    background-color: rgb(77,199,55);
}


</style>




<div bp="grid">

<div bp = "offset-5@md 4@md 12@sm" class="progress-container">

<div class="progress-bar" style="width:{progress}">



    <span class="sr-only">{progress}</span>
</div>


</div>

</div>

