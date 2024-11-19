<script>
import MainComponent from './components/MainComponent.vue';
import Footer from './components/partials/Footer.vue';
import Header from './components/partials/Header.vue';

export default {
  name: "Vite-Boolfolio",
  components: {
    MainComponent, 
    Footer,
    Header
},
};



</script>

<template>
 
 <Header />

 <MainComponent />

<Footer />

</template>

<style lang="scss">

</style>
