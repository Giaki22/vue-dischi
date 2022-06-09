<template>
    <div class="container-albums">
        <ul>
            <li v-for="(album, i) in filterAlbums" :key="i">
                <AalbumCard :album="album"></AalbumCard>
            </li>
        </ul>
    </div>
</template>

<script>
import axios from 'axios';
import AalbumCard from '../Atoms/AalbumCard.vue';
import data from '../../shared/data.js'

export default {
    name: "McontainerAlbum",
    data() {
        return {
            albums: [],
            data
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((reply) => {
            this.albums = reply.data.response;
        });
    },
    computed: {
        filterAlbums() {
            if (data.filterValue == '') {
                return this.albums
            } else {
                return this.albums.filter(albums => albums.genre.toLowerCase() == data.filterValue.toLowerCase());
            }
        }
    },
    components: { AalbumCard }
}

</script>

<style scoped>
.container{
    display: flex;
    flex-flow: row wrap;
}
ul{
    list-style: none;
    display: flex;
    flex-flow: row wrap;
    gap: .625rem;
}
li{
    background-color: #2e3a46;
    width: calc(100% / 5 - .625rem);
}
</style>