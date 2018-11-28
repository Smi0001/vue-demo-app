<template>
    <div class="container">
        <div class="row text-left">
            <div class="col-md-5">
                <div class="panel panel-primary">
                    <div class="panel-heading">
                        <h6 class="panel-title">Binding, v-for, v-model, v-on:click, v-on:input, v-bind:class</h6>
                    </div>
                    <div class="panel-body">
                        <div class="form-group">
                            <i class="fas m-rl-5 fa-2x add-tags fa-plus-circle text-success cur-p" v-on:click="setTags()"></i>
                            <input type="text" class="form-control" placeholder="Type tags & press Enter" v-model="tagItem" v-on:input="setTags2($event)" >
                        </div>
                    </div>
                </div>
                <div class="panel panel-success">
                    <div class="panel-body">
                        Tags: <span class="text-primary"> {{tagItem}} </span>
                    </div>
                </div>
            </div>
            <div class="col-md-7">
                <div class="d-flex flex-wrap">
                    <div class="p-2 btn" v-for="(item, index) in tagArray" :key='index' v-bind:class="{ 'bg-warning': (index%2 === 0), 'bg-info': (index%2 !== 0) }">{{index}}. {{item}}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            tagItem: '',
            tagArray: [],
        };
    },
    methods: {
        setTags2(event) {
            if (event.keycode === 13) {
                this.tagArray.push(this.tagItem);
                this.tagItem = '';
            }
        },
        setTags() {
            if (this.tagItem !== '') {
                this.tagArray.push(this.tagItem);
                this.tagItem = '';
            }
        },
    },
};
</script>

<style>
    .text-left {
        text-align: left;
    }
    input {
        max-width: 300px;
    }
    .add-tags {
        position: absolute;
        right: 100px;
    }
</style>
