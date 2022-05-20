<template>  
  <div class="container mt-5">
    <div class="ms_container">
    <div v-if="loading">
    <AppLoading />
    </div>
     <div v-else class="row row-cols-5">
       <AppAlbumCard v-for="(item, index) in albums" :key="index" :album="item"/>
     </div> 

    </div>
  </div>
</template>

<script>
import AppAlbumCard from './AppAlbumCard.vue'
import AppLoading from './AppLoading.vue'
import AppSelect from './AppSelect.vue'
import axios from "axios"

export default {
    name: "AppCardList",
    components: {
        AppAlbumCard,
        AppLoading,
        AppSelect
    },
    data() {
      return {
        albums: [],
        loading: true
      }
    },
    created() {
      axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.albums = resp.data.response;
        this.loading = false
      }
      )
    }
}
</script>

<style lang="scss" scoped>
.ms_container {
  width: 70%;
  margin: 0 auto;
}
</style>