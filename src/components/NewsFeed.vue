<template>
  <div class="newsfeed">
    <h3>This is the news feed</h3>
    <div class="peeps">
      <div class="peep">
       {{ data }}
      </div>        
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsFeed',
  data() {
    return {
      data: {}
    }
  },
    beforeMount() {
    this.getPeep();
  },
  methods: {
    async getPeep() {
      const res = await fetch("https://jsonplaceholder.typicode.com/comments");
      const data = await res.json();
      
      const result = data.map(comments => 
        comments.map(comment => comment.body)
        )
      
      this.data = result

      
    }
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
