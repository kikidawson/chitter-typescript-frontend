<template>
  <div class="newpeep">
    <h1>{{ newPeep }}</h1>

    <form id="newpeep-form">
      <label class="newpeep-form-lable"></label>
      <textarea class="input" name="body" placeholder="What's on your mind?"/>
      <input type="submit" name="submit" value="Peep">  
    </form>

  </div>
</template>

<script>
export default {
  name: 'NewPeep',
  props: {
    newPeep: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
