<template>
  <div id="app">
    <AppHeader />
    <AppSong />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppSong from './components/AppSong.vue'


export default {
  name: 'App',
  components: {
    AppHeader,
    AppSong,
}
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

</style>
