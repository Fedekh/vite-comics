<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";
import AppFeatures from "./components/AppFeatures.vue";

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
    AppFeatures
  }
}
</script>

<template>
  <div class="main-container">
    <div class="main-wrapper">
      <AppHeader />
      <AppContent />
      <AppFeatures />
      <AppFooter />
    </div>
  </div>
</template>


<style lang="scss">
@use "./style/general.scss" as *;

body {
  .container {
    width: 100%;
    height: 100vh;
  }
}
</style>


<!--? In SCRIPT importo qualsiasi componente Vue che scriverò poi lo esporto nella key specifica "components", usando lo stesso name di riferimento (good practies). Nel TEMPLATE, che è da considerare come il body del nostro progetto finale, immettero tramite self-closing pseudotag. con lo stesso nomeche è in script. Nello STYLE importo lo style general, e se serve gli stili singoli se dovessi scrivere altro css al di fuori di quello general -->