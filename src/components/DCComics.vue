<script>
export default {
    name: "DCComics",
}
</script>


<template>
    <main class="flex align-center justify-center">
        <div class="col-10 m-center">
            --> Content goes here <--
        </div>
    </main>
</template>


<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

main {
    background-color: $brand_secondary;
    height: 150px;
    color: white;
}
div {
    text-align: center;
}
</style>