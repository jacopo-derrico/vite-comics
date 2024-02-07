<script>

export default {
    name: "DCFooterIcon",
    data() {
        return {
            socialIcons: [
                {
                    link: '#',
                    icon: 'footer-facebook.png',
                },
                {
                    link: '#',
                    icon: 'footer-twitter.png',
                },
                {
                    link: '#',
                    icon: 'footer-youtube.png',
                },
                {
                    link: '#',
                    icon: 'footer-pinterest.png',
                },
                {
                    link: '#',
                    icon: 'footer-periscope.png',
                }
            ]
        }
    }
}

</script>

<template>
    <footer>

        <div class="container">

            <div>
                <button>Sign-up now!</button>
            </div>

            <div class="socials">
                <h3>Follow us</h3>
                <ul>
                    <li v-for=" (element, index) in socialIcons" :key="index">
                        <a href="element.link">
                            <img :src="`./src/assets/img/${element.icon}`" alt="Social Icon" width="30">
                        </a>
                    </li>
                </ul>
            </div>

        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

footer {

    background-color: $footer_color;
    padding-block: 40px;

    .container {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            border: 2px solid $brand_primary;
            background-color: rgba(0, 0, 0, 0);
            color: white;
            padding: 10px 20px;
            font-size: 1rem;
            text-transform: uppercase;
            cursor: pointer;
        }

        .socials {
            display: flex;
            gap: 30px;
            align-items: center;

            h3 {
                color: $brand_primary;
                text-transform: uppercase;
                font-size: 1.5rem;
                font-weight: 700;
            }

            ul {
                display: flex;
                gap: 20px;

                li {
                    list-style: none;
                }
            }
        }
    }
}
</style>