<template>
    <div class="container">
        <h1>Vue Counter</h1>
        <p>{{ count }}</p>
        <button @click="increment">Increment</button>
        <button @click="decrement">Decrement</button>
    </div>
</template>

<script>
    export default {
        name: 'Counter',
        data() {
            return {
                count: 0
            }
        },
        methods: {
            increment() {
                this.count++
            },
            decrement() {
                this.count--
            }
        }
    }
</script>

<style scoped>
.container {
    text-align: center;
    color: #2c3e50;
    margin: 0 auto;
}
</style>