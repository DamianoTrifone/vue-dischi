<template>
  <div class="copertine">
        <Search @selectGender="onSelectGender" />
        <div
            class="card_container"
            v-for="(album, index) in filteredAlbums" 
            :key="index"
        >
            <Album :item="album" />
        </div>
  </div>
</template>
 
<script>
import axios from 'axios';
import Album from "./Album.vue";
import Search from "./Search.vue";

export default {
    name: "Albums",
    components: {
        Album,
        Search
    },
    data: function () {
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albums: [],
            genre: 'all'
        }
    },
    created: function(){
        axios
            .get(this.apiUrl)
            .then((response) => {
                this.albums = response.data.response;
            })
    },

    methods: {
        onSelectGender: function(payload){
            this.genre = payload;
        }
    },

    computed: {
        filteredAlbums: function (){
            if (this.genre !== 'all') {
                return this.albums.filter(album =>{
                    return album.genre.toLowerCase().includes(this.genre.toLowerCase())
                })
            } else {
                return this.albums;
            }
        }
    }
}
</script>

<style>

</style>