<script>
export default {
    name: "AppFooter",
    data() {
    }
} 
</script>

<template>
    <div class="pippo"></div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.pippo {
  width: 100%;
  height: 400px;
  background-image: url(../assets/img/dc-logo-bg.png), url(../assets/img/footer-bg.jpg);
  background-position: center right, center center;
  background-repeat: no-repeat, repeat;
  background-size: calc(45%), cover;
  
}


</style>