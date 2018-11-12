<template>
  <div id="navbar" class="navbar">
    <div class="navflex">
      <a href="/" class="na">
          <img class="logo hidden" src="./assets/logo.png" id="brand">
          <img class="logo" src="./assets/white-logo.png" id="white_brand">
      </a>
      <a href="/" class="na">dev.About()</a>
      <a href="/" class="na">dev.Projects()</a>
      <a href="/" class="na">dev.Contact()</a>
      <a href="/" class="na">dev.Topper()</a>
      <a v-on:click="open" class="na icon"> &#9776; </a>
    </div>
    
    <Sidenav ref="sidenav"></Sidenav>
  </div>
</template>

<script>
  import Sidenav from './Sidenav.vue'
  
  export default {
    name: 'Navigation',
    components: { 'Sidenav': Sidenav },
    methods: {

      open: function() {
        this.$refs.sidenav.open();
      },

      animationTrigger: function() {
        var anchors = document.querySelectorAll(".navbar .na");

        if(window.scrollY > 20) {
          navbar.style.background = "white";
          navbar.style.boxShadow = "0px 3px 5px #666";
          brand.style.display = "block";
          white_brand.style.display = "none";

          for(var i = 0, len = anchors.length; i < len; i ++)
            anchors[i].style.color = '#999';
        }

        else {
          navbar.style.background = "transparent";
          navbar.style.boxShadow = "none";
          white_brand.style.display = "block";
          brand.style.display = "none";

          for(var i = 0, len = anchors.length; i < len; i ++)
            anchors[i].style.color = 'white';
        }
      }
    },

    created () {
      window.addEventListener('scroll', this.animationTrigger);
    },

    destroyed () {
      window.removeEventListener('scroll', this.animationTrigger);
    }
  }

</script>

<style lang="scss">

  .navbar {
    width: 100%;
    position: fixed;
    top: 0px;
    transition: .5s;
  }

  .navbar .navflex {
    width: 70%;
    display: inline-flex;
    flex-flow: row nowrap;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0px 20px 50px;
  }

  .navbar .na {
    color: white;
    font-size: 20px;
    cursor: pointer;
    text-decoration: none;
  }

  .navbar .na.icon {
    display: none !important;
  }

  .logo {
    height: 60px;
  }

  .hidden {
    display: none;
  }

  @media screen and (max-width: 1007px) {
    .navbar .navflex { width: 90% }
    .navbar .na:not(:first-child) { display: none; }
    .navbar .na.icon {
      display: inline-flex !important;
      float: right;
    }
  }

  @media screen and (max-width: 470px) {   
    .navbar .na.icon {
      display: inline-flex !important;
    }

  }

</style>
