<template>
    <McontainerAlbum></McontainerAlbum>
</template>

<script>
import McontainerAlbum from '../Molecules/McontainerAlbum.vue';

export default {
    name: 'ObaseMain',
    components: { McontainerAlbum }
}
</script>

<style scoped>
    .container-albums{
        margin: auto;
        margin-top: 3.125rem;
        width: 70%;
    }
</style>