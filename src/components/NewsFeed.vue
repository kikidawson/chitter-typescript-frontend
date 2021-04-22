<template>
  <div class="newsfeed">
    <h3>This is the news feed</h3>
    <div class="peeps">
      <div class="peep"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsFeed',
  props: {
      peeps: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
a {
  color: #42b983;
}
</style>
