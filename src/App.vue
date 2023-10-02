<template>
  <div class="app">
    <counterView :counter="counter"></counterView>
    <buttonView :counter="counter" :pace="pace" @increment="increment"></buttonView>
  </div>
</template>

<script>
import counterView from '@/components/counterView.vue'
import buttonView from './components/buttonView.vue';
import {ref} from 'vue'
export default {
  components:{
      counterView,
      buttonView
    },
  setup(){
    let counter = ref(100);
    let pace = ref(2);
    const increment = (smcounter)=>{
      counter.value = smcounter
    }
    return {counter,pace,increment}
  }
}
</script>

<style lang="scss">

</style>
