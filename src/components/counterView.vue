<template>
    <div>
        {{ counter }}
    </div>
</template>

<script>
export default {
    components: {},
    props: {
        counter: {
            type: Number,
            default: 0,
            required: true
        }
    },
}
</script>
<style scoped>

</style>