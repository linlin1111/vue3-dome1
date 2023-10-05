<template>
  <div class="app">
    <p>error</p>
    <!-- 显示数据组件 -->
    <counterView :num="num"></counterView>
    <!-- 显示按钮组件 -->
  
import {ref} from 'vue'
export default {
  components:{
      counterView,
      buttonView
    },
  setup(){
    let num = ref(150)
    let pace = 2
    const getNewNum = (newNum)=>{
      console.log(newNum)
      num.value = newNum
    }
    return {
      num,getNewNum,pace
    }
  }
}
</script>

<style lang="scss">

</style>
