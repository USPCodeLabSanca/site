<template>
  <div id="sidenav" class="sidenav">
    <div class="sideheader">
      <img class="sidelogo" src="./assets/clean-logo.png" alt="logo"/>
    </div>
    <a v-on:click="close" class="sa closebtn"> &times; </a>
     <div class="sidebody"> 
      <a href="/" class="sa">dev.About()</a>
      <a href="/" class="sa">dev.Projects()</a>
      <a href="/" class="sa">dev.Contact()</a>
      <a href="/" class="sa">dev.Topper()</a>
    </div>  
  </div>
</template>

<script>
  export default {
    name: 'Sidenav',
    methods: {
      open: function() {

        var anchors = document.querySelectorAll(".sidenav .sa");

        sidenav.style.width = "50%";

        for(var i = 0, len = anchors.length; i < len; i ++)
          anchors[i].style.display = 'block';   
      },

      close: function() {  
        var anchors = document.querySelectorAll(".sidenav .sa");

        sidenav.style.width = "0px";

        for(var i = 0, len = anchors.length; i < len; i ++)
          anchors[i].style.display = 'none';
      },
    }
  }
</script>

<style>

  .sidenav {
    width: 0;
    height: 100%;
    display: flex;
    flex-flow: column nowrap;
    align-items: flex-start;
    align-content: space-around;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    background-color: white; 
    transition: margin-left 0.5s;
    box-shadow: 0px 3px 5px #666;
    overflow-x: hidden;
  }

  .sidenav .sideheader {
    width: 100%;
    height: 20%; 
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    background-image: linear-gradient(#d7f4ef, #72d8ca);
  }

  .sidenav .sa .sidebody {
    width: 100%;
    height: 40%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-around;
  }

  .sidenav .closebtn {
    position: absolute;
    font-size: 36px !important;
    color: white !important;
    align-self: flex-end;
  }

  .sidenav .sa {
    padding: 8px 8px 8px 20px;
    text-decoration: none;
    font-size: 18px;
    color: #999 !important;
    cursor: pointer;
    display: none;
    transition: .5s;
  }

  .sidenav .sa:hover {
    color: #666;
  }

  .sidelogo {
    border-radius: 50%;
    background: white;
    height: 70px;
  }

/*.sidenav {
    height: 100%; 
    width: 0; 
    position: fixed; 
    z-index: 1; 
    top: 0; 
    left: 0;
    background-color: white; 
    padding-top: 20px; 
    transition: margin-left 0.5s;
    box-shadow: 0px 3px 5px #666;
    opacity: .95;
    overflow-x: hidden;
  }

  .sidenav .sideul .sideli {
    padding: 8px 8px 8px 0px;
    text-align: left;
    text-decoration: none;
    font-size: 18px;
    color: #999 !important;
    cursor: pointer;
    display: none;
    transition: .5s;
  }

  .sidenav .closebtn {
    position: absolute;
    top: 0;
    right: 25px;
    font-size: 36px !important;
    margin-left: 50px;
  }

  .sidelogo {
    border-style: solid;
    border-color: #00c9ae;
    border-width: 2px;
    border-radius: 50%;
    background: white;
    height: 50px;
  }*/

</style>