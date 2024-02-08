<script>
export default {
    name: "DCSlides",
    props: {
        propsSrc: String,
        propsSeries: String,
    }
}
</script>


<template>
    <div>
        <figure>
            <img :src="propsSrc" :alt="propsSeries">
        </figure>
        <h4 class="uppercase">{{ propsSeries }}</h4>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;


div {
    figure {
        width: 100%;
        margin-bottom: 20px;
        overflow: hidden;

        img {
            width: 100%;
            display: block;
            object-fit: cover;
            aspect-ratio: 1;
        }

        &:hover img {
            scale: 1.3;
            transition: scale 0.5s ease-in-out;
        }
    }
}
</style>