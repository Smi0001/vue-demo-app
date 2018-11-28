<template>
    <div class="container">
        <div class="row text-left">
            <div class="col-md-5">
                <div class="panel panel-primary">
                    <div class="panel-heading">
                        <h6 class="panel-title">Binding, v-for, v-model, Key Modifiers(@keyup.enter), Event Modifiers(v-on:click.stop), v-bind:class</h6>
                    </div>
                    <div class="panel-body">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Type tags & press Enter" v-model="tagItem" @keyup.enter="setTags()" >
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
                    <div class="p-2 btn" v-for="(item, index) in tagArray" :key='index' v-bind:class="{ 'bg-warning': (index%2 === 0), 'bg-info': (index%2 !== 0) }">{{index}}. {{item}}
                        <span class="close-icon" style="display: inline-block;" v-on:click.stop="remove"> x</span>
                    </div>
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
        setTags: function() {
            if (this.tagItem !== '') {
                this.tagArray.push(this.tagItem);
                this.tagItem = '';
            }
        },
        remove: function(event) {
            event.target.parentElement.remove();
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
    .close-icon {
        padding: 5px;
        margin-left: 10px;
        text-transform: uppercase;
        font-size: 10px;
        border-left: 1px solid #a5a5a5;
    }
</style>
