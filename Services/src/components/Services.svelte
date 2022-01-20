<script>

    export let head;
    export let servicesText;
</script>


<style>




.text-container {
    
    margin-left: 125px;
    padding-bottom: 40px;
    width: auto;
    text-align: center;
    
}


.text {
    
    width: 400px;
    
}

.text-header {
    
    
    color:red;
    
}

.services-text {
    display: flex;
    
}


</style>




<div class="text-container">

    <div class="text">
      <h1 class="text-header">{head}</h1>
      <p class="services-text">
        {servicesText}
      </p>
    </div>
</div>


