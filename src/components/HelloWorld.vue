<template>
<div>
  <div class="hello">
     <button v-on:click="counter += 1">+</button>
    <span>{{ counter }}</span>
    <button v-on:click="counter -= 1">-</button>
  </div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return  {counter:0}
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
