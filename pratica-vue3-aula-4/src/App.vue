<template>
    <TheHeader v-if="showHeader" />
  <!-- v-show==> serve para esconder elemento da pagina(se usa quando quer remover element e não remover no codigo)-->
    <div v-show="showName">
      <!--Declaração de varaiavel {{ firstName }} no template-->
        Nome: {{ firstName }} <br>
        Sobrenome: {{ lastName }}
    </div>
<!-- v-if==> serve para esconder elemento da pagina(se usa quando quer remover element e codigo)-->
    <div v-if="accessLevel === 'admin'">Usuário Admin</div>
    <div v-else-if="accessLevel === 'marketing'">Usuário Marketing</div>
    <div v-else>Usuário normal</div>

    <img
        alt="Vue logo"
        src="./assets/logo.png"
    >
  <TheHome />
    <div style="padding-left:20px">
      <h1>Responsive Header</h1>
      <p>Resize the browser window to see the effect.</p>
      <p>Some content..</p>
    </div>
  <TheHome />

  <TheFooter/>
</template>

<script>
import TheHome from './components/TheHome.vue'
import TheHeader from './components/TheHeader';
import TheFooter from './components/TheFooter';

export default {
    name: 'App',
    components: {
        TheHome,
        TheHeader,
        TheFooter
    },
    data() {
        return {
            showHeader: true,
            firstName: 'Jon',
            lastName: 'Snow',
            showName: false,
            accessLevel: 'admin'
        }
    }
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
