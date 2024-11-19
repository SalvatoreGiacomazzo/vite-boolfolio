<script>

import axios from 'axios';

export default {
name:"MainComponent",
data(){
    return {
        wantedList : [],

    }

    },  methods:{
getWantedList(){
    axios.get('http://127.0.0.1:8000/api/wanted')
  .then ((response) =>{
      
          this.wantedList = response.data.results
   console.log(this.wantedList);
   
  })
  .catch(function (error) {
   
    console.log(error);
  })




}


}, mounted(){
    this.getWantedList();
}



}

</script>

<template>
<div class="container justify-content-center align-items-center">
    <div class="row">
        <div class="col-12">
<div class="card" style="width: 18rem;">
  <img class="card-img-top" src="..." alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
</div>
</div>
</div>
</template>


<style lang="scss">

</style>