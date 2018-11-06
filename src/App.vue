<template>
  <div id="app">
    <Navigation></Navigation>
    <Banner></Banner>
    <div style="height: 300px;">
      
    </style>
      
    </div>
  </div>
</template>

<script>
  import Navigation from './Navigation.vue'
  import Banner from './Banner.vue'
  export default {
    name: 'app',
    components: {
      'Navigation': Navigation,
      'Banner': Banner
    }
  }
</script>

<style>

  body {
    margin: 0;
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

</style>