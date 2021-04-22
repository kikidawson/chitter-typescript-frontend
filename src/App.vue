<template>
  <div id="app">
    <NewPeep />
    <NewsFeed />
  </div>
</template>

<script>
import NewPeep from './components/NewPeep.vue'
import NewsFeed from './components/NewsFeed.vue'

export default {
  name: 'App',
  components: {
    NewPeep,
    NewsFeed
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
