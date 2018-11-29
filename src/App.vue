<template>
  <div id="app">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/fontawesome.css" integrity="sha384-u5J7JghGz0qUrmEsWzBQkfvc8nK3fUT7DCaQzNQ+q4oEXhGSx+P2OqjWsfIRB8QT" crossorigin="anonymous">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/solid.css" integrity="sha384-rdyFrfAIC05c5ph7BKz3l5NG5yEottvO/DQ0dCrwD8gzeQDjYBHNr1ucUpQuljos" crossorigin="anonymous">
    <marquee behavior="alternate" class="logo-div">
      <img alt="Vue logo" title="Vue logo" src="./assets/logo.png" class="logo">
    </marquee>
  <hr>
    <Ether msg="Click events handling"/>
  <hr> 
    <Form />
  <hr> 
    <Computed counter="0" />
  </div>
</template>

<script lang="ts">
import Ether from './components/Ether.vue';
import Form from './components/Form.vue';
import Computed from './components/Computed.vue';

export default {
  name: 'app',
  components: {
    Ether,
    Form,
    Computed,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.logo-div {
  left: 0;
  position: absolute;
  top: 0;
}
.logo {
  height: 55px;
  width: auto;
  margin: 5px;
}
</style>
