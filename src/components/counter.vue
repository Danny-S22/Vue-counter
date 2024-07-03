<template>
    <div class="container">
        <h1 id="title">Vue Counter</h1>
        <p id="counter">{{ count }}</p>
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
#title {
    font-size: 5rem;
    color: black;
}

#counter {
    font-size: 3rem;
    color: black;
}

.container {
    text-align: center;
    margin: 25vh auto;
}
</style>    