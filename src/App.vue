<template>
  <div id="app">
   <AppHeader />
   <AppCardList />
   <AppAlbumCard />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppCardList from './components/AppCardList.vue'
import AppAlbumCard from './components/AppAlbumCard.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppCardList,
    AppAlbumCard
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
