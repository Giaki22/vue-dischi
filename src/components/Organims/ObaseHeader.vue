<template>
    <div class="container">
        <AbaseLogo></AbaseLogo>
        <AselectionFilter></AselectionFilter>
    </div>
</template>

<script>
import AbaseLogo from '../Atoms/AbaseLogo.vue';
import AselectionFilter from '../Atoms/AselectionFilter.vue';

export default {
    name:'ObaseHeader',
    components: {
    AbaseLogo,
    AselectionFilter
}
}
</script>

<style scoped>
.container{
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    align-items: center;
    color: white;
    background-color: #2e3a46;
    height: 3.75rem;
    padding: .625rem;
}
</style>