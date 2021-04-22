<template>
  <div class="newsfeed">
    <h3>This is the news feed</h3>
    <div class="peeps">
      <div id='example-1'>
        <ul>
          <li v-for="comments in data" :key='comments'>{{ comments.id }}. {{ comments.body }}</li>
        </ul>   
      </div>
    </div>
  </div>
</template>

<script>
// import Vue from 'vue';

export default {
  name: 'NewsFeed',
  data() {
    return {
      data: {}
    }
  },
  beforeMount() {
    this.getPeeps();
  },
  methods: {
    async getPeeps() {
      const res = await fetch("https://jsonplaceholder.typicode.com/comments");
      const data = await res.json();
      this.data = data;
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
</style>
