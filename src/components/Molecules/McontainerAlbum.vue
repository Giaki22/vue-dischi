<template>
    <div class="container-albums">
        <ul>
            <li v-for="(album, i) in albums" :key="i">
                <AalbumCard :album="album"></AalbumCard>
            </li>
        </ul>
    </div>
</template>

<script>
import axios from 'axios';
import AalbumCard from '../Atoms/AalbumCard.vue';

export default {
    name: "McontainerAlbum",
    data() {
        return {
            albums: []
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((reply) => {
            this.albums = reply.data.response;
        });
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