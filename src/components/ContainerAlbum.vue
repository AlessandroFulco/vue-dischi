<template>
    <div>
        <MySelected
        @mySearch="inputGenere"
        />
        

        <section class="container-album">

    
        <AlbumCard
            v-for="(album, index) in filteredGenre" :key="index"
            :albumData="album"
        />
    </section>
    </div>
    
</template>

<script>
import axios from "axios"
import AlbumCard from "./AlbumCard.vue"
import MySelected from "./MySelected.vue"

export default {
    name: 'ContainerAlbum',
    components: {
    AlbumCard,
    MySelected
},
    data(){
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albumAuthor: [],
            userText : "",
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
        inputGenere(genereUser) {
            this.userText = genereUser;
        }
    },
    computed: {
        filteredGenre(){
            if ( this.userText === "all") {
                return this.albumAuthor;
            }   else {
                return this.albumAuthor.filter(item => {
                    return item.genre.toLowerCase().includes(this.userText.toLowerCase());
                });
            }
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .container-album{
        padding: 50px;
        margin: 0 auto;
        width: 70%;
        height: calc(100vh - 100px);
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: flex-start;
        gap: 20px;
    }
</style>
