<script>
import DCHeader from './components/DCHeader.vue'
import DCComics from './components/DCComics.vue'
import DCIconBanner from './components/DCIconBanner.vue'
import DCFooter from './components/DCFooter.vue'

import '@fontsource/pt-sans-narrow/400.css';
import '@fontsource/pt-sans-narrow/700.css';

export default {
    components: {
        DCHeader,
        DCComics,
        DCIconBanner,
        DCFooter
    }
}
</script>


<template>
    <DCHeader />
    <DCComics />
    <DCIconBanner />
    <DCFooter />
</template>


<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
@use "./styles/partials/mixins" as *;
</style>
