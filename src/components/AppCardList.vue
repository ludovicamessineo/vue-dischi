<template>  
  <div class="container mt-5">
     <div class="row row-cols-5 g-2">
       <AppAlbumCard v-for="(item, index) in albums" :key="index" :album="item"/>
     </div> 
  </div>
</template>

<script>
import AppAlbumCard from './AppAlbumCard.vue'
import axios from "axios"

export default {
    name: "AppCardList",
    components: {
        AppAlbumCard
    },
    data() {
      return {
        albums: []
      }
    },
    created() {
      axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.albums = resp.data.response;
      }
      )
    }
}
</script>

<style lang="scss" scoped>

</style>