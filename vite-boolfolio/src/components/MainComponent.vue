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
    <div class="container d-flex justify-content-center align-items-center flex-wrap">
      <div class="row justify-content-center ">
        <div class="col-4 mb-4" v-for="wanted in wantedList" :key="wanted.id">
          <div class="card" style="width: 24rem;">
            <img class="card-img-top" src="https://wallpapercave.com/wp/wp7819542.jpg" alt="Card image cap">
            <div class="card-body">
              <h5 class="card-title">{{ wanted.name }} {{ wanted.last_name }}</h5>
              <p class="card-text"><strong>In the State of:</strong>{{wanted.nationality}}</p>
      <p class="card-text"><strong>Most Used Device:</strong>{{wanted.device.device_type}}</p>
      <p class="card-text">
              <strong>Wanted for the crime of:</strong>
                <ul>
                  <li v-for="felony in wanted.felonies" :key="felony.id">{{ felony.name }}</li>
                </ul>
      </p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>


<style lang="scss">


ul{
    list-style-type: none;
}


</style>