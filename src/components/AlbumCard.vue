<template>
    <figure class="album">
        <img :src="albumData.poster" :alt="albumData.title">
        <figcaption>
            <h2>{{albumData.title}}</h2>
            <span>
                {{albumData.author}}
                <br>
                {{albumData.genre}}
            </span>
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
    .album {
        flex-basis: calc((100% - 100px) / 5);
        min-height: 350px;
        background-color: #2e3a46;
        margin-bottom: 20px;
        img {
            padding-top: 20px;
            max-width: 150px;
            height: auto;
        }
        figcaption {
            h2 {
                text-transform: uppercase;
            margin-top: 20px;
            color: #fff;
            }
            span {
                font-weight: bold;
                display: inline-block;
                margin-top: 20px;
                color: #aaa;
            }
        }
    }
</style>
