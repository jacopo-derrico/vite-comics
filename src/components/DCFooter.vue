<script>
export default {
    name: "DCFooter",
    data() {
        return {
            comicsMenu: [
                {
                    name: 'characters',
                    link: '#'
                },
                {
                    name: 'comics',
                    link: '#'
                },
                {
                    name: 'movies',
                    link: '#'
                },
                {
                    name: 'TV',
                    link: '#'
                },
                {
                    name: 'games',
                    link: '#'
                },
                {
                    name: 'videos',
                    link: '#'
                },
                {
                    name: 'news',
                    link: '#'
                },
            ],
            shopMenu: [
                {
                    name: 'shop DC',
                    link: '#'
                },
                {
                    name: 'shop DC collectibles',
                    link: '#'
                },
            ],
            dcMenu: [
                {
                    name: 'terms of use',
                    link: '#'
                },
                {
                    name: 'privacy policy (new)',
                    link: '#'
                },
                {
                    name: 'ad choices',
                    link: '#'
                },
                {
                    name: 'advertising',
                    link: '#'
                },
                {
                    name: 'jobs',
                    link: '#'
                },
                {
                    name: 'subscriptions',
                    link: '#'
                },
                {
                    name: 'talent workshops',
                    link: '#'
                },
                {
                    name: 'CPSC certificates',
                    link: '#'
                },
                {
                    name: 'ratings',
                    link: '#'
                },
                {
                    name: 'shop help',
                    link: '#'
                },
                {
                    name: 'contact us',
                    link: '#'
                },
            ],
            sitesMenu: [
                {
                    name: 'DC',
                    link: '#'
                },
                {
                    name: 'DC MAD magazine',
                    link: '#'
                },
                {
                    name: 'DC kids',
                    link: '#'
                },
                {
                    name: 'DC universe',
                    link: '#'
                },
                {
                    name: 'DC power visa',
                    link: '#'
                },
            ]
        }
    },
}
</script>


<template>
    <footer class="w-100">
        <div class="container flex m-center col-10 ">
            <div class="flex-column">
                <nav class="col-10 m-center">
                    <h4 class="uppercase">dc comics</h4>
                    <ul class="flex-column">
                        <li v-for="(element, index) in comicsMenu">
                            <a href="{{ element.link }}" class="capitalize">{{ element.name }}
                            </a>
                        </li>
                    </ul>
                </nav>
                <nav class="col-10 m-center">
                    <h4 class="uppercase">shop</h4>
                    <ul class="flex-column">
                        <li v-for="(element, index) in shopMenu">
                            <a href="{{ element.link }}" class="capitalize">{{ element.name }}
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
            <div>
                <nav class="col-10 m-center">
                    <h4 class="uppercase">dc</h4>
                    <ul class="flex-column">
                        <li v-for="(element, index) in dcMenu">
                            <a href="{{ element.link }}" class="capitalize">{{ element.name }}
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
            <div>
                <nav class="col-10 m-center">
                    <h4 class="uppercase">sites</h4>
                    <ul class="flex-column">
                        <li v-for="(element, index) in sitesMenu">
                            <a href="{{ element.link }}" class="capitalize">{{ element.name }}
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>

        <figure class="floating-logo">
            <img src="../assets/img/dc-logo-bg.png" alt="dc logo">
        </figure>
    </footer>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-size: cover;
    position: relative;
    padding-block: 40px;
    overflow: hidden;


    .container {
        justify-content: start;
        gap: 20px;
    }

    h4 {
        color: white;
        font-size: 25px;
        margin-bottom: 10px;
    }

    ul {
        margin-bottom: 10px;

        a {
            color: gray;
            font-size: 12px;
        }
    }

    .floating-logo {
        position: absolute;
        transform: translateY(-50%);
        top: 50%;
        right: 10%;
    }
}
</style>