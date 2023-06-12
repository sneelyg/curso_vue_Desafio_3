<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <AButton @clickHijo="padreHandleClick" />
  <div>
    <NewComponent :titulo="'Test de compomnentes con CLI'" 
    :subtitulo="'Esto podría ser un subtítulo'"
    :datos= '[2, 4, 6, 8, 10]' 
    titulo_tabla="Tabla de números pares"
    />
    <NewComponent 
    :titulo="'Y esta es la otra tabla:'" 
    :subtitulo="'pero sin subtítulo'" 
    :datos= '[1, 3, 5, 7, 9]'
    titulo_tabla="Tabla de números impares" />
  </div>
</template>

<script>
import NewComponent from './components/NewComponent.vue';



export default {
  name: 'App',
  components: {

    NewComponent,

  },
  methods: {
    padreHandleClick() {
      console.log("Click en el Padre")

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
