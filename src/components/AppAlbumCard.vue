<template>
  <div class="card text-center p-3">
      <img :src="album.poster" alt="">
      <h2>{{ album.title }}</h2>
      <small>{{ album.author }}</small>
      <small>{{ album.year }}</small>
  </div>
  
</template>

<script>
export default {
    name: "AppAlbumCard",
    props: {
      album: Object
    }
    
}
</script>

<style lang="scss" scoped>
.card {

  background-color: #2e3a46;
  color: grey;

  h2 {
    font-size: .9rem;
    color: white;
    margin-top: .5rem;
  }
}
</style>