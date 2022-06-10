<template>
    <section class="container-album">
        <AlbumCard
            v-for="(album, index) in albumAuthor" :key="index"
            :albumData="album"
        />
    </section>
</template>

<script>
import axios from "axios"
import AlbumCard from "./AlbumCard.vue"
export default {
    name: 'ContainerAlbum',
    components: {
        AlbumCard
    },
    data(){
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albumAuthor: []
        }
    },
    created() {
        this.getAlbum()
    },
    methods: {
        getAlbum() {
            axios
            .get(this.apiUrl)
            .then(result => {
                this.albumAuthor = result.data.response;
                console.log(result);
            })
            .catch(error => {
                console.log("Errore", error);
            })
        },
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .container-album{
        padding: 50px;
        margin: 0 auto;
        width: 70%;
        height: 100vh;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;
    }
</style>
