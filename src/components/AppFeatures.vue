<script>
export default {
    name: "AppFeatures",
    data() {
    },
    methods: {
        getImgPath(name) {
            return new URL(`../assets/img/${name.img}`, import.meta.url).href;
        }
    }
} 
</script>

<template>
   <div class="features"></div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;
.features{
    width: 100%;
    height: 150px;
    background-color: $mainblu;
    }
</style>
