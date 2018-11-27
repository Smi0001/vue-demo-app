<template>
    <div class="container text-left">
        <div class="panel panel-primary">
            <div class="panel-heading">
                <h3 class="panel-title">Binding</h3>
            </div>
            <div class="panel-body">
                <form>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Type your name" v-model="name" >
                    </div>
                    <div class="form-group">
                        <input type="text" class="form-control" placeholder="Type your email" v-model="email" >
                    </div>
                </form>
            </div>
        </div>

        <div class="panel panel-success">
            <div class="panel-body">
                Name: {{name}}
                <br>
                Email: {{email}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
        };
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
</style>
