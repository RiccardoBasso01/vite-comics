<script>
export default {
    data() {
        return {
            imgNames: [
                {
                    url: 'footer-facebook.png',
                },
                {
                    url: 'footer-periscope.png',
                },
                {
                    url: 'footer-pinterest.png',
                },
                {
                    url: 'footer-twitter.png',
                },
                {
                    url: 'footer-youtube.png',
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
    <div class="upper-footer">
        <div class="container-xl">
            <div class="footer-nav">
                <div>

                    <h4>DC COMICS</h4>
                    <ul>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>
                    <h4>SHOP</h4>
                    <ul>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC Collectibles</a></li>
                    </ul>
                </div>

                <div>
                    <h4>DC</h4>
                    <ul>
                        <li><a href="#">Term of use</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Add Choice</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact us</a></li>
                    </ul>

                </div>
                <div>
                    <h4>SITES</h4>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <div class="bottom-footer">
        <div class="container-xl">
            <div class="bottom-nav">
                <button>SIGN-UP NOW!</button>
                <div class="links-social">
                    <h4>FOLLOW US</h4>
                    <ul>
                        <li v-for="imgName in this.imgNames">
                            <a href="#"><img :src="getImagePath(imgName.url)" :alt="imgName.url"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/style.scss' as *;
@use '../assets/scss/_colors.scss' as *;

.upper-footer {
    background-image: url(../assets/img/dc-logo-bg.png), url(../assets/img/footer-bg.jpg);
    background-position: right 15% center, center;
    background-size: auto 500px, cover;
    background-repeat: no-repeat, no-repeat;
    height: 400px;
    overflow: hidden;
    color: white;
    padding-top: 20px;
}

h4 {
    margin: 20px 0;
}

li {
    font-size: 13px;
    font-weight: 200;
    color: grey;
}

.footer-nav {
    display: flex;
    gap: 20px;
}

.bottom-footer {
    background-color: $darkGrey;
    padding: 20px;
}

button {
    color: white;
    border: 2px solid $primaryColor;
    padding: 10px;
    font-weight: 700;
    font-size: 20px;

    &:hover {
        background-color: $primaryColor;
    }
}

.bottom-nav {
    display: flex;
    justify-content: space-between;
}

.links-social {
    display: flex;

    h4 {
        color: $primaryColor;
    }

    ul {
        display: flex;
        align-items: center;
        gap: 20px;
        margin-left: 20px;
    }
}
</style>