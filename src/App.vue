<script>
import DCHeader from './components/DCHeader.vue'
import DCComics from './components/DCComics.vue'

import '@fontsource/pt-sans-narrow/400.css';
import '@fontsource/pt-sans-narrow/700.css';

export default {
    components: {
        DCHeader,
        DCComics
    }
}
</script>


<template>
    <DCHeader />
    <DCComics />
    <!-- <DCFooter /> -->
</template>


<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
@use "./styles/partials/mixins" as *;
</style>
