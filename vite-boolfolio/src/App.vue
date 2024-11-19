<script>
import CardList from './components/CardList.vue';
import Footer from './components/partials/Footer.vue';
import Header from './components/partials/Header.vue';

export default {
  name: "Vite-Boolfolio",
  components: {
    CardList, 
    Footer,
    Header
},
};



</script>

<template>
 
 <Header />

 <CardList />

<Footer />

</template>

<style lang="scss">

</style>
