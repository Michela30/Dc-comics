<script>
//import
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';


   export default {
    data() {
      return{

      }
    },
    components: {
      HeaderComponent,
      MainComponent,
      FooterComponent
    },
  }
</script>



<template>
  <div>

    <HeaderComponent/>

    <MainComponent/>

    <FooterComponent/>

  </div>
</template>




<style lang="scss">
@use 'assets/scss/main.scss';
@use 'assets/scss/variables.scss';




</style>
