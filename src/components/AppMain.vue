<script>
export default {
    data() {
        return {
            imgNames: [
                {
                    url: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    url: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    url: 'buy-comics-shop-locator.png',
                    text: 'SUBSCRIPTION'
                },
                {
                    url: 'buy-comics-subscriptions.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    url: 'buy-dc-power-visa.svg',
                    text: 'COMIC SHOP LOCATOR'
                }
            ]
        };
    },
    methods: {
        getImagePath(imgName) {
            const url = new URL(`../assets/img/${imgName}`, import.meta.url)
            return url.href
        }
    }
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


    <div class="main-nav">
        <div class="container-xl">
            <ul>
                <li v-for="imgName in this.imgNames">
                    <a href="#"><img :src="getImagePath(imgName.url)" :alt="imgName.text"></a>
                    <a href="#">{{ imgName.text }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_colors.scss' as *;
@use '../assets/scss/style.scss' as *;

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

.main-nav {
    background-color: $primaryColor;
}

ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
}

li {
    padding: 20px 0;
    display: flex;
    align-items: center;
    font-size: 10px;
    gap: 10px;
    color: white;
}

img {
    height: 50px;
    width: auto;
}

li:last-child img {
    width: 50px;
}
</style>