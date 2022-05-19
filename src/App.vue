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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
