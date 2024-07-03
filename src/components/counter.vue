<template>
    <div class="container">
        <h1 id="title">Vue Counter</h1>
        <p id="counter">{{ count }}</p>
        <button class="btn btn-primary btn-dark" @click="increment">Increment</button>
        <button class="btn btn-primary btn-dark" @click="reset">Reset</button>
        <button class="btn btn-primary btn-dark" @click="decrement">Decrement</button>
    </div>
</template>

<script>
    export default {
        name: 'Counter',
        data() {
            return {
                count: parseInt(localStorage.getItem('count')) || 0
            }
        },
        methods: {
            increment() {
                this.count++;
                this.storeCounterSetting();
            },
            decrement() {
                this.count--;
                this.storeCounterSetting();
            },
            reset () {
                this.count = 0;
                this.storeCounterSetting();
            },
            storeCounterSetting () {
                localStorage.setItem('count', this.count);
            },
        },
    }
</script>

<style scoped>
button {
    font-size: 1.3rem;
    margin: 1rem;
}

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