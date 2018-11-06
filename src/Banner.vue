<template>
  <div id="banner" class="banner">
    <div class="flex-container">
      <div class="flex-box50">
        <h1 class="title">USPCodeLab Sanca</h1>
        <span class="welcome-text">
          Versão mais gostosa do USPCodeLab, xupa ime. Nós também fazemos projetos muito sérios.
        </span>
      </div>
      <div class="flex-box50">
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
    height: 800px;
    /*background-image: linear-gradient(#4d4d4d, #333);*/
    background-image: linear-gradient(#72d8ca, #00c9ae);
  }

  .im {
    border-image: white;
    border-radius: 50%;
    background: white;
    height: 400px;
  }

  .flex-container {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-around;
    padding: 150px 70px 0px 70px;
    align-items: flex-start;
  }

  .flex-box50 {
    display: flex;
    flex-wrap: wrap;
  }

  .title {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    font-weight: 400;
    font-size: 50px;
    color: white;
    padding-top: 100px;
  }

  .welcome-text {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    font-weight: 100;
    font-size: 25px;
    color: white;
    padding: 0px 100px 0px 0px;
  }

</style>