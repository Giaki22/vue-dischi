<template>
    <div class="container">
        <AbaseLogo></AbaseLogo>
    </div>
</template>

<script>
import AbaseLogo from '../Atoms/AbaseLogo.vue';

export default {
    name:'ObaseHeader',
    components: {
        AbaseLogo
    }
}
</script>

<style scoped>
.container{
    background-color: #2e3a46;
    height: 3.75rem;
    padding: .625rem;
}
</style>