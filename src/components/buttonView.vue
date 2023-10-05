<template>
    <div>
        <button @click="jisuan(pace)">+</button>
        <button @click="jisuan(-pace)">-</button>
    </div>
</template>

<script>
export default {
   props:{
    pace:{
        type:Number,
        required:true,
        default:1
    },
    num:{
        type:Number,
        required:true,
    }
   },
   setup(props,{emit}){
    let newNum = 0
    const jisuan = (pace)=>{
        newNum = props.num+pace
        emit('newNum',newNum)
    }

    return {
        jisuan
    }
   }
   
}
</script>
<style scoped>

</style>