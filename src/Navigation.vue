<template>
  <div id="navbar" class="navbar">
    <ul>
      <li><img class="logo" src="./assets/logo.png" id="brand"></li>
      <li>dev.Home()</li>
      <li>dev.About()</li>
      <li>dev.Contact()</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Navigation',
    methods: { 
      animationTrigger: function() {
        var anchors = document.querySelectorAll(".navbar ul li");

        if(window.scrollY > 50) {
          navbar.style.background = "white";
          navbar.style.boxShadow = "0px 3px 5px #1a1a1a";

          for(var i = 0, len = anchors.length; i < len; i ++)
            anchors[i].style.color = '#999';       
        }

        else {
          navbar.style.background = "transparent";
          navbar.style.boxShadow = "none";

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

  .navbar ul li {
    list-style-type: none;
    display: inline-block;
    padding: 10px 50px;
    font-size: 20px;
    color: white;
    font-family: sans-serif;
    cursor: pointer;
    transition: .5s;
    vertical-align: middle;
  }

  .navbar ul li:hover {
    color: #1a1a1a;
  }

  .logo {
    height: 50px;
  }

</style>
