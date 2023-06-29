<script>
export default {
    data() {
        return {};
    },
}
</script>

<template>
    <!-- main -->
    <div class="jumbotron">
        <div class="container-xl">
            <div class="jumbo-content">
                <h2 class="jumbo-title">The Flash</h2>
            </div>
        </div>
    </div>

    <div class="container-xl">
        <h2>Contennuto principale</h2>
    </div>
</template>

<style lang="scss" scoped>
.jumbotron {
    height: 500px;
    background-image: url(../assets/img/jumbotron.avif);
    background-position: center;
    background-size: cover;
    box-shadow: 0px -20px 100px 10px black inset;
}

.jumbo-content {
    height: 480px;
    display: flex;
    align-items: flex-end;
}

.jumbo-title {
    color: white;
    font-size: 40px;
    margin-bottom: 50px;
}
</style>