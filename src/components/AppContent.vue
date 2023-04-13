<script>
export default {
    name: "AppContent",
    data() {
    }
} 
</script>

<template>
    <div class="wrapper-title">
        <section class="title">
            <h1>CONTENT GOES HERE</h1>
        </section>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.wrapper-title {
    height: 120px;
    width: 100%;
    background-color: $mainblack;
    color: white;
    .title{
        @include ms_container(120px, 0 auto);
        @include flex(row, flex-start, center);

    }

}
</style>
