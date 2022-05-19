<template>
  <div id="app">
    <header>
      <AppHeader />
    </header>

    <main>
      <AppSong />
    </main>
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
