<script>
export default {
    name: "AppContent",
    data() {
    }
} 
</script>

<template>
    <div class="container-content">

        <h1>CONTENT GOES HERE</h1>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.container-content{
    background-color: $textcolor;
    height: 120px;
    @include flex(row, flex-start, center);
    h1{
        @include ms_container;
    }
}
</style>
