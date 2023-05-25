<template>
    <div>
        <h2>{{ cardWords }}</h2>
        <p>This is my car !</p>
        <button @click="resetMyCar()">Change my Car !</button>
    </div>
</template>
<script>
export default {
    props: {
        cardWords: {
            type: String,
            default: null,
        },
    },
    methods: {
        resetMyCar(){
            this.$emit('resetMyCar');
        }
    },
}
</script>
<style scoped>
    div {
        padding: 30px;
        margin: 0 auto;
        border: 1px solid red;
        text-align: center;
    }
    
</style>