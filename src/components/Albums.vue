<template>
  <div class="copertine">
    <div
        class="card_container"
        v-for="(album, index) in albums" 
        :key="index"
    >
        <Album :item="album" />
    </div>
  </div>
</template>
 
<script>
import axios from 'axios';
import Album from "./Album.vue";

export default {
    name: "Albums",
    components: {
        Album
    },
    data: function () {
        return {
            apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
            albums: [],
        }
    },
    created: function(){
        axios
            .get(this.apiUrl)
            .then((response) => {
                this.albums = response.data.response;
                console.log(this.albums);
            })
    }
}
</script>

<style>

</style>