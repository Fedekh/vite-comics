<script>
export default {
    name: "AppLocandine",
    props:{
        immagine: String,
        prezzo: String,
        serie: String,
        nomefumetto: String
    },
    
} 
</script>

<template>
    <div class="card">
        <img :src="immagine" :alt="serie">
        <h4>{{ nomefumetto }}</h4>
        <h5>{{ prezzo }}</h5>
    </div>

</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.card{
    width: calc(100% / 6 - 10px);
    margin: 5px;
    padding: 10px;
    background-color: rgba(93, 138, 146, 0.397);
    border-radius: 20px;
    position: relative;
    cursor: pointer;
    img{
        width: 100%;
        height: 70%;
    }
    h4, h5{
        color: rgb(243, 243, 243);
        position: absolute;
        // bottom: 25px;
    }
    h5{
        bottom: 10px;
        color: rgb(21, 255, 0);

    }
}   
</style>