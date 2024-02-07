<script>
export default {
    name: "DCIconBanner",
    data() {
        return {
            bannerLink: [
                {
                    name: 'digital comics',
                    link: '#',
                    image: 'buy-comics-digital-comics.png'
                },
                {
                    name: 'dc merchandise',
                    link: '#',
                    image: 'buy-comics-merchandise.png'
                },
                {
                    name: 'subscription',
                    link: '#',
                    image: 'buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    link: '#',
                    image: 'buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    link: '#',
                    image: 'buy-dc-power-visa.svg'
                },
            ]
        }
    }
}
</script>


<template>
    <div>
        <nav class="h-100 col-10 m-center flex align-center">
            <ul class="flex h-100 w-100 align-center m-center">
                <li v-for="(element, index) in bannerLink" class="h-100 flex align-center">
                    <figure>
                        <img :src="`./src/assets/img/${element.image}`">
                    </figure>
                    <a href="{{ element.link }}" class="uppercase">{{ element.name }}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

div {
    background-color: $brand_primary;
    height: 150px;
}

nav {
    ul {
        margin-block: 50px;
        justify-content: space-around;

        li {
            figure {
                width: 50px;
            }

            img {
                object-fit: cover;
            }

            a {
                color: white;
                margin-left: 25px;
            }
        }

        li:nth-child(1), li:nth-child(4) figure{
            height: 50px;
        }
        li:nth-child(1), li:nth-child(4) figure img{ 
            width: auto;
            height: 100%;
        }
    }
}
</style>