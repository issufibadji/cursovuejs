<template>
    <TheHeader />

    <img
        alt="Vue logo"
        src="./assets/logo.png"
    >
    <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
//importação de componentes
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader';

export default {
    name: 'App',
  //declaração de componentes que serão utilizados
    components: {
        HelloWorld,
        TheHeader
    },
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
