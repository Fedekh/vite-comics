<script>
import AppHeader from "./components/AppHeader.vue";
export default {
    components:{
        AppHeader
    }
}
</script>

<template>
  <div class="container">
    <div class="wrapper">
      <AppHeader/>
    </div>
  </div>
  </template>


<style lang="scss">
@use "./style/general.scss" as *;

body{
  background-color: rgb(114, 113, 116);
  .container{
    width: 100%;
    height: 100vh;
    .wrapper{
      width: 80%;
      margin: 0 auto;
    }
  }
}


</style>


<!--? In SCRIPT importo qualsiasi componente Vue che scriverò poi lo esporto nella key specifica "components", usando lo stesso name di riferimento (good practies). Nel TEMPLATE, che è da considerare come il body del nostro progetto finale, immettero tramite self-closing pseudotag. con lo stesso nomeche è in script. Nello STYLE importo lo style general, e se serve gli stili singoli se dovessi scrivere altro css al di fuori di quello general -->