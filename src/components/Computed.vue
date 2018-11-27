<template>
    <div class="text-left container">
        <h3>Counter computed:
            {{view}}
            <i class="fas m-rl-5 fa-plus-circle text-success cur-p" v-on:click="counter++"></i>
            <i class="fas m-rl-5 fa-minus-circle text-danger cur-p" v-on:click="counter--"></i>
        </h3>
    </div>
</template>

<script>

export default {
    data() {
        return {
            counter: 0,
        };
    },
    computed: {
        view() {
            return this.counter < 0 ? 0 : this.counter;
        },
    },
};
</script>

<style>
    .m-rl-5 {
        margin: 5px;
    }
    .cur-p {
        cursor: pointer;
    }
    .text-success:hover {
        color: #1c7e33 !important;
    }
    .text-danger:hover {
        color: #640912 !important;
    }
</style>
