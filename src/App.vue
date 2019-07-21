<template>
  <div class="hello">
    <div>
      <input id="count" v-model.number="num"/>
      <CounterGroup :CounterNum="num"></CounterGroup>
    </div>
  </div>
</template>

<script>
import Counter from './components/Counter.vue'
import CounterGroup from './components/CounterGroup.vue'
export default {
  name: 'app',
  props:{

  },
  components: {
    Counter,
    CounterGroup
  },
  data(){
    return{
      num:0
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
