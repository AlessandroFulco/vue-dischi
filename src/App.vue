<template>
  <div id="app">
    <ContainerAlbum/>
  </div>
</template>

<script>
import ContainerAlbum from './components/ContainerAlbum.vue'

export default {
  name: 'App',
  components: {
    ContainerAlbum
  }
}
</script>

<style lang="scss">
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
