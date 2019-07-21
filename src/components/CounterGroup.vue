<template>
<div>
  <div v-for="n of CounterNum" :key="n">
    <Counter 
      @increase="increaseNum"
      @decrease="decreaseNum">
    </Counter>
  </div>
  <CounterSum :counterSum="sum"></CounterSum>
</div>
</template>

<script>
import Counter from "./Counter.vue";
import CounterSum from "./CounterSum.vue";

export default {
  name:'CounterGroup',
  props:['CounterNum'],
  components:{
    Counter,
    CounterSum
  },
  data(){
     return {
       sum:0
      }
  },
  methods:{
    increaseNum(){
      this.sum++
    },
    decreaseNum(){
      this.sum--
    }
  }
}
</script>

<style>

</style>
