<template>
    <div>
        {{ num }}
    </div>
</template>

<script>
export default {
    props:{
        num :{
            type:Number,
            required:true,
            default:200
        }
    }
}
</script>
<style scoped>

</style>