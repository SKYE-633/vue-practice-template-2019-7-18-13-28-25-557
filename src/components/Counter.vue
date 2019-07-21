<template>
<div>
  
    <button @click="increase">+</button>
    <span>{{ counter }}</span>
    <button @click="decrease">-</button>

</div>
</template>

<script>
export default {
  name: 'Counter',
  props:{
    msg:String
  },
  data(){
    return  {
      counter:0
      }
  },
  methods:{
    increase(){
      this.counter++,
      this.$emit("increase");
    },
    decrease(){
      this.counter--,
      this.$emit("decrease");
    }
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
