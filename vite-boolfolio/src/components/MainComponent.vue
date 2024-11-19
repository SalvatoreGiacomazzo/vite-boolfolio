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
  .then(function (response) {
    
    console.log(response.data.results);
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

<h2 class="text-warning">Hello Vue</h2>

</template>


<style lang="scss">

</style>