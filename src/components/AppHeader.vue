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
    <header>
        <div class="container-xl">
            <div class="d-flex">
                <div class="logo">
                    <a href="#"><img src="dc-logo.png" alt="logo"></a>
                </div>

                <ul class="navbar d-none">
                    <li v-for="link in this.links" :class="{ active: link.current }">
                        <a href="#">{{ link.text.toUpperCase() }}</a>
                    </li>
                </ul>

            </div>
            <div class="center-Y gap-3">
                <div>
                    <a href="#"><img src="../assets/img/search_icon.png" alt="search-icon"></a>
                </div>

                <div class="hamburger-menu">
                    <a href="#"><img src="../assets/img/hamburger-menu.png" alt="hamburger-menu" title="hamburger-menu"></a>
                </div>

                <ul class="navbar d-none">
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
    background-color: white;
    position: sticky;
    top: 0;
    left: 0;
    z-index: 1;
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
    height: 60px;
    padding: 0 10px;
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
    }
}
</style>