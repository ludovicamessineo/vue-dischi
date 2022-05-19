<template>
  <div class="card text-center">
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
  h2 {
    font-size: .9rem;
  }
}
</style>