<template>
  <div id="app">
    <ObaseHeader></ObaseHeader>
    <ObaseMain></ObaseMain>
  </div>
</template>

<script>
import ObaseHeader from './components/Organims/ObaseHeader.vue';
import ObaseMain from './components/Organims/ObaseMain.vue';

export default {
    name: "App",
    components: { ObaseHeader, ObaseMain }
}
</script>

<style lang="scss">
@import './assets/style/global-parts/reset';
body{
  background-color: #1e2d3b;
}
</style>
