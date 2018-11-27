<template>
    <div class="container text-left">
        <span>{{ msg }} {{ price }}</span>
        <button class="btn" @click="decrease()">Decrement</button>
        <button class="btn" @click="increase()">Increment</button>
    </div>
</template>

<script>
export default {
    name: 'Ethereum',
    data() {
        return {
            price: 500,
        };
    },
    methods: {
        decrease() {
            this.price = this.price - 1;
        },
        increase() {
            this.price = this.price + 1;
        },
    },
    props: {
        msg: String,
    },
};
</script>

<style>
    .btn {
        margin: 5px;
        padding: 3px 5px;
        color: #000;
        background: #79d5f7;
        /* border: 1px solid black; */
        border-radius: 5px;
    }
    .btn:active {
        box-shadow: 2px 4px;
        -webkit-box-shadow: 1px 3px;
        -moz-box-shadow: 1px 3px;
        /* background: #0d7499; */
        /* color: #fff; */
    }
</style>
