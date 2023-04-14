<script>
export default {
    name: "AppLocandine",
    props:{
        immagine: String,
        prezzo: String,
        serie: String,
        tipo: String
    },
    data() {
        return {
           
   
}}
} 
</script>

<template>
    <div class="card">
        <img :src="immagine" :alt="serie">
        <h5>{{ tipo }}</h5>
        <h4>{{ prezzo }}</h4>
    </div>

</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.card{
    width: calc(100% / 6 - 10px);
    margin: 5px;
    padding: 10px;
    img{
        max-width: 100%;
    }
}
</style>