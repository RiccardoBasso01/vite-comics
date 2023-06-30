<script>
export default {
    data() {
        return {
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ],
        };
    },
}
</script>

<template>
    <!-- header -->
    <header>
        <div class="container-xl">

            <div class="navbar">
                <div class="logo">
                    <a href="#"><img src="dc-logo.png" alt="logo"></a>
                </div>

                <div>
                    <ul>
                        <li v-for="link in this.links" :class="{ active: link.current }">
                            <a href="#">{{ link.text.toUpperCase() }}</a>
                        </li>
                    </ul>
                </div>

            </div>
            <div class="navbar">
                <ul>
                    <li><a href="#"><img src="../assets/img/search_icon.png" alt="search-icon"></a></li>
                    <li><a href="#">SIGN UP</a></li>
                    <li><a href="#">LOG IN</a></li>
                </ul>
            </div>

        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss' as *;
@use '../assets/scss/_colors.scss' as *;

header {
    display: block;
    font-size: 13px;
    font-weight: 900;
    position: sticky;
    top: 0;
    left: 0;
    background-color: white;
}

ul {
    display: flex;
}


li {
    height: 60px;
    display: flex;
    align-items: center;
    margin-right: 20px;
    position: relative;

    &.active {
        color: $primaryColor;
    }

    &:hover {
        color: $primaryColor;
    }
}


li.active::after,
li:hover::after {
    content: '';
    width: 100%;
    height: 3px;
    background-color: $primaryColor;
    position: absolute;
    bottom: 0;
    left: 0;
}

.container-xl {
    display: flex;
    justify-content: space-between;
    padding: 0;
}

.navbar {
    height: 60px;
    display: flex;
    align-items: center;
}

img {
    width: 24px;
}

.logo {
    display: flex;
    align-items: center;

    img {
        width: 40px;
        margin-right: 40px;
        display: block;
    }
}
</style>