<template>
    <div>
        header
        <p>{{ myName }}</p>
        <p>firstName: {{ firstName }}</p>
        <p>lastName:{{ lastName }}</p>
        <p>age:{{ age }}</p>
        <p v-for="(student, index) in students" :key="index">{{ student }}</p>
        <button @click="updateName">Click me</button>
        <hr>
    </div>
</template>

<script>
export default {
    props : {
        myName : {
            type: String,
            default: ''
        },
        students: {
            type: Array,
            default: null
        },
        firstName: String,
        lastName: String,
        age: Number,
    },
    methods: {
        updateName() {
            let updateName = this.firstName === 'John' ? 'Shahnewaz' : 'John'
            this.$emit('updateValue', updateName);
        }
    }
}
</script>

<style scoped>
    div { 
    color: red;
    }
</style>