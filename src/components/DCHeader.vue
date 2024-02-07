<script>
export default {
    name: "DCHeader",
    data() {
        return {
            navLink: [
                {
                    name: 'charachters',
                    link: '#',
                    current: false
                },
                {
                    name: 'comics',
                    link: '#',
                    current: true
                },
                {
                    name: 'movie',
                    link: '#',
                    current: false
                },
                {
                    name: 'tv',
                    link: '#',
                    current: false
                },
                {
                    name: 'games',
                    link: '#',
                    current: false
                },
                {
                    name: 'collectibles',
                    link: '#',
                    current: false
                },
                {
                    name: 'videos',
                    link: '#',
                    current: false
                },
                {
                    name: 'fans',
                    link: '#',
                    current: false
                },
                {
                    name: 'news',
                    link: '#',
                    current: false
                },
                {
                    name: 'shop',
                    link: '#',
                    current: false
                }
            ]
        }
    }
}
</script>


<template>
    <header class="flex col-10">
        <figure>
            <img src="../assets/img/dc-logo.png" alt="DC logo">
        </figure>

        <nav class="h-100">
            <ul class="flex h-100">
                <li v-for="(element, index) in navLink" class="h-100 flex align-center"
                    :class="element.current ? 'active-underline' : ''">
                    <a href="{{ element.link }}" :class="element.current ? 'active' : ''">{{ element.name }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

header {
    justify-content: space-between;
    align-items: center;
    height: 80px;
    margin: 20px auto;

    figure {
        height: 80px;
    }

    img {
        width: 80px;
    }

    ul {
        gap: 20px;
    }

    a {
        text-transform: uppercase;
        color: $brand_secondary;
        display: block;
    }

    li:has(> a:hover) {
        border-bottom: 5px solid $brand_primary;
        padding-top: 0.3rem;
    }

    li {
        list-style: none;
    }
}
</style>
