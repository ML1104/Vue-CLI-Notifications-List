<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1 {
  color: white;
}

.hello {
  width: 50%;
  margin-left: 25%;
  border: 1px solid black;
  text-align: center;
  background-color: brown;
}


</style>
