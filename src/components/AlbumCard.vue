<template>
    <figure class="figure">
        <img :src="albumData.response.poster" :alt="albumData.response.title">
        <figcaption>
            <h2></h2>
            <div></div>
            <div></div>
        </figcaption>
    </figure>
</template>

<script>

export default {
    name: 'AlbumCard',
    props: {
        albumData: Object
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    h3 {
        margin: 40px 0 0;
    }
</style>
