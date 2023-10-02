<template>
    <div>
        <button @click="increment(mspace)">+</button>
        <button @click='increment(-mspace)'>-</button>
    </div>
</template>

<script>
import {ref} from 'vue'
export default {
    components: {},
    props:{
        counter: {
            type: Number,
            default: 0,
            required: true
        },
        pace:{
            type: Number,
            default: 0,
            required: true
        }
    },
    setup(props,{emit}){
        let mspace = ref(props.pace)
        let mscounter = ref(props.counter)
        const increment = (inc)=>{
            mscounter.value+=inc
            emit("increment",mscounter.value)
        }
        return {increment,mspace,mscounter}
    }
}
</script>
<style scoped>

</style>