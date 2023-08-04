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


  <TheHome />
    <div style="padding-left:20px">
      <h1>Responsive Header</h1>

      <div
          v-for="(obj, index) in todos"
          v-bind:key="obj.id"
          class="todos-item"
      >
        {{ index}} - {{ obj.title }}
      </div>
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
            accessLevel: 'admin',
          todos: [
            {
              "userId": 1,
              "id": 1,
              "title": "delectus aut autem",
              "completed": false
            },
            {
              "userId": 1,
              "id": 2,
              "title": "quis ut nam facilis et officia qui",
              "completed": false
            },
            {
              "userId": 1,
              "id": 3,
              "title": "fugiat veniam minus",
              "completed": false
            },
            {
              "userId": 1,
              "id": 4,
              "title": "et porro tempora",
              "completed": true
            },
            {
              "userId": 1,
              "id": 5,
              "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
              "completed": false
            }
          ]
        }
    }
}
</script>

<style>
.todos-item {
  background: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;
  text-align: left;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px;
}


</style>
