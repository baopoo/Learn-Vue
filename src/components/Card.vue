<template>
    <div>
        <h2>{{ cardWords }}</h2>
        <p>{{ msg }}</p>
        <button @click="resetMyCar()">Change my Car !</button>
        <button @click="changeMsg()">Change message</button>
    </div>
</template>
<script>
export default {
    props: {
        cardWords: {
            type: String,
            default: null,
        },
        msg: {
            type: String,
            default: null,
        },
        changeMsg: Function
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