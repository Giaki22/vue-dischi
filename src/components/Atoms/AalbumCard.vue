<template>
  <div class="album">
      <img :src="album.poster" alt="">
      <h4>{{album.title}}</h4>
          <h5 class="author">{{album.author}}</h5>
          <h5 class="date">{{album.year}}</h5>
  </div>
</template>

<script>
export default {
    name:'AalbumCard',
    props:{
        album: Object,
    }
}
</script>

<style scoped lang="scss">
.album{
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    padding: 1.25rem;
    gap: .625rem;
    img{
        width: 100%;
        aspect-ratio: 1/1;
    }
    h4{
        text-align: center;
        text-transform: uppercase;
        color: white;
    }
    h5{
        text-align: center;
        color: #7b726a; 
    }
}
</style>