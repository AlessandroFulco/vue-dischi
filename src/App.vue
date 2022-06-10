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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #1e2d3b;
}
</style>
