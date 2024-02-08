<script>
import DCSlides from './DCSlides.vue'
export default {
    name: "DCComics",
    components: {
        DCSlides
    },
    data() {
        return {
            slidesComics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    }
}
</script>


<template>
    <main>
        <div class="banner w-100 ">
            <div class="uppercase title">current series</div>
        </div>
        <div class="col-10 m-center">
            <div id="slider" class="flex">
                <DCSlides class="slide" v-for="(element, index) in slidesComics" :key="index" :propsSrc="element.thumb"
                    :propsSeries="element.series" />
            </div>
            <div class="flex justify-center">
                <button class="uppercase">load more</button>
            </div>
        </div>
    </main>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

main {
    background-color: $brand_secondary;
    color: white;

    .banner {
        background-image: url(../assets/img/jumbotron.jpg);
        background-position: top;
        background-size: cover;
        position: relative;
        height: 350px;

        .title {
            position: absolute;
            padding: 15px;
            background-color: $brand_primary;
            bottom: calc((-1rem/2) - 8px);
            left: calc($single-col - 10px);
            font-weight: 700;
            font-size: 20px;
        }
    }
}

#slider {
    flex-wrap: wrap;
    gap: 15px;
    margin-block: 50px 20px;
}

.slide {
    flex-basis: calc((100% / 6) - 15px);
    margin-bottom: 30px;
}

button {
    border: none;
    background-color: $brand_primary;
    padding: 10px;
    color: white;
    margin-bottom: 30px;
}
</style>