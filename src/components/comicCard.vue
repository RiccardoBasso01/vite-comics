<script>
export default {
    data() {
        return {

        };
    },

    props: {
        comics: Array
    },


    methods: {
        getImagePath(imgUrl) {
            const url = new URL(imgUrl, import.meta.url)
            return url.href
        }
    }
}

</script>

<template>
    <div class="comics">
        <ul>
            <li v-for="comic in comics">
                <a href="#">
                    <img :src="getImagePath(comic.thumb)" :alt="comic.series">
                    <!-- <span>{{ comic.series }}</span> -->
                </a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_colors.scss' as *;
@use '../assets/scss/style.scss' as *;

$numberOfCols: 2;
$spacing: 10px;



// cols

li {
    width: calc(100% / $numberOfCols);
    padding: 0 $spacing;
    margin: $spacing 0;
}

// row
ul {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -$spacing;
    margin: - $spacing 0;
}

a {
    display: block;
}

@media screen and (min-width: 576px) {
    $numberOfCols: 3;

    li {
        width: calc(100% / $numberOfCols);
    }
}

@media screen and (min-width: 768px) {
    $numberOfCols: 4;

    li {
        width: calc(100% / $numberOfCols);
    }
}

@media screen and (min-width: 992px) {
    $numberOfCols: 6;

    li {
        width: calc(100% / $numberOfCols);
    }
}
</style>