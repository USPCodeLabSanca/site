<template>
  <div id="banner" class="banner">
    <div class="fluid-container">
      <div class="half-container">
        <h1 class="title">USPCodeLab Sanca</h1>
      </div>
      <div class="half-container">
        <img class="im" src="./assets/clean-logo.png" alt="logo"> 
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Banner'
  }
</script>

<style>

  .banner {
    width: 100%;
    height: auto;
    padding: 50px;
    background-image: linear-gradient(#72d8ca, #00c9ae);
  }

  .fluid-container {
    width: 100%;
    height: auto;
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
  }

  .im {
    border-image: white;
    border-radius: 50%;
    background: white;
    width: 80%;
    height: auto;
  }

/*  .flex-container {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    padding: 150px 100px 0px 80px;
    align-items: flex-start;
  }*/


  /*.flex-box50 {
    display: flex;
    flex-wrap: wrap;
  }*/

  .half-container {
    width: 50%;
    height: auto;
    display: flex;
    flex-flow: column wrap;
    align-items: center;
    justify-content: flex-start;
    padding: 100px;
  }

  .title {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    font-weight: 400;
    font-size: 50px;
    color: white;
    padding-top: 80px;
  }

</style>