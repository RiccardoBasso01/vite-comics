<script>
import comicCard from './comicCard.vue';

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
            ],
            comics: [
                {
                    thumb:
                        'https://static.dc.com/2023-06/BM-TBATB_Cv2_00211_DIGITAL_C1.jpg?w=640',
                    price: '$19.99',
                    series: 'Batman: The brave and the bold #2 ',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/OU2E3_3vA7flyv-SJ3TcFW1d99KDlp5ZfmW9ylLLFDo/rs:fit:1012:1200:1/g:ce/aHR0cHM6Ly9pMC53/cC5jb20vd3d3LnN1/cGVycG91dm9pci5j/b20vd3AtY29udGVu/dC91cGxvYWRzLzIw/MjAvMDcvQW1lcmlj/YW4tVmFtcGlyZS0x/OTc2LTAxLWNvdi1B/bGJ1cXVlcnF1ZS0y/MDIwLmpwZz9yZXNp/emU9MTAxMiUyQzE1/NTYmc3NsPTE',
                    price: '$3.99',
                    series: 'American Vampire 1976',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/gAZQuZyt6WjcUWF6aXCIBaiJqtOJAK-X4nxS9Vbvwno/rs:fit:1200:1200:1/g:ce/aHR0cHM6Ly9jZG4y/LnBlbmd1aW4uY29t/LmF1L2NvdmVycy9v/cmlnaW5hbC85Nzgx/NDAxMjc1NDI2Lmpw/Zw',
                    price: '$16.99',
                    series: 'Aquaman',
                    type: 'graphic novel',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/YET9wY29Aa29TyHqlbieS9qsz3HWyNYQx-WkRqdBRX4/rs:fit:640:984:1/g:ce/aHR0cDovL2dldHlv/dXJjb21pY29uLmNv/LnVrL3dwLWNvbnRl/bnQvdXBsb2Fkcy8y/MDE2LzA4L2JhdGdp/cmwtcmViaXJ0aC0x/LWNvdmVyLmpwZw',
                    price: '$2.99',
                    series: 'Batgirl',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://static.dc.com/2023-06/TD_ROBIN_CV10_01011_DIGITAL.jpg?w=640',
                    price: '$3.99',
                    series: 'Tim Drake: Robin',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/jgxYlrx442aozemzjqdmCsd9DkIkRollJp1T8sG8TfE/rs:fit:720:1106:1/g:ce/aHR0cHM6Ly9veXN0/ZXIuaWduaW1ncy5j/b20vd29yZHByZXNz/L3N0Zy5pZ24uY29t/LzIwMTgvMTAvU1RM/MDk3MDk1LTcyMHgx/MTA2LmpwZw',
                    price: '$2.99',
                    series: 'Batman Beyond',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://static.dc.com/2023-06/BMTACS3_Cv6_00611_DIGITAL.jpg?w=640',
                    price: '$3.99',
                    series: 'Batman: The adventures continue season three ',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://static.dc.com/2023-06/TfDkCr%20%28%20Cover%29.jpg?w=640',
                    price: '$4.99',
                    series: 'Tales from dark crisis',
                    type: 'graphic novel',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/kSLCPBIeE9s218LRC4cIyrHOYmxrSS2Wt7LvNNfED2I/rs:fit:455:700:1/g:ce/aHR0cHM6Ly9jb21p/Y2Jvb2tyZWFsbS5j/b20vY292ZXItc2Nh/bi81ZmFmMTFjYTk1/NGQ1MGVjZDA1ZmU3/M2U1NjBiNWQyOC94/bC8tLWlzc3VlLTEu/anBn',
                    price: '$5.99',
                    series: 'Batman: The Joker War Zone',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/a6fAPUra4t94xMJFlYv6X7Lwm4z_qPmslx7Hiqafbok/rs:fit:600:923:1/g:ce/aHR0cHM6Ly9jZG4u/ZmxpY2tlcmluZ215/dGguY29tL3dwLWNv/bnRlbnQvdXBsb2Fk/cy8yMDIwLzA4L0Jh/dG1hbi1UaHJlZS1K/b2tlcnMtMS02MDB4/OTIzLTEuanBn',
                    price: '$6.99',
                    series: 'Batman: Three Jokers',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://imgs.search.brave.com/qMxyCwK99aguaETp4ioxXLrpxwNg2JNBN3Oq7LGAgzM/rs:fit:780:1200:1/g:ce/aHR0cHM6Ly9jZG4u/ZmxpY2tlcmluZ215/dGguY29tL3dwLWNv/bnRlbnQvdXBsb2Fk/cy8yMDIwLzEwL0Jh/dG1hbi1XaGl0ZS1L/bmlnaHQtUHJlc2Vu/dHMtSGFybGV5LVF1/aW5uLTEtMS5qcGc',
                    price: '$4.99',
                    series: 'Batman: White Knight Presents: Harley Quinn',
                    type: 'comic book',
                },
                {
                    thumb:
                        'https://static.dc.com/2023-06/GA_Cv3_00311_DIGITAL.jpg?w=640',
                    price: '$16.99',
                    series: 'Green arrow',
                    type: 'comic book',
                },
            ]
        };
    },

    components: { comicCard },

    methods: {
        getImagePath(imgName) {
            const url = new URL(`../assets/img/${imgName}`, import.meta.url)
            return url.href
        }
    }
}
</script>

<template>
    <div class="jumbotron">
        <div class="container-xl">
            <div class="jumbo-content">
                <h2 class="jumbo-title">The Flash</h2>
            </div>
        </div>
    </div>

    <div class="comics-list">
        <div class="container-xl">
            <div class="comics-title">
                <h3>LATEST COMICS & GRAPHIC NOVELS</h3>
            </div>
            <comicCard :comics="this.comics" />
        </div>
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
    font-family: $openSans;
}

img {
    height: 50px;
    width: auto;
}

li:last-child img {
    width: 50px;
}

.comics-title {
    background-color: $primaryColor;
    color: white;
    padding: 10px;
    font-size: 20px;
    display: inline-block;
    translate: 0 -50%;
}

.comics-list {
    background-color: $darkGrey;
}
</style>