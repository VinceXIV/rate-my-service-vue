<template>
  <NavBar/>
  <CanvasComponent :objectArray="data"  />
</template>

<script>
import NavBar from './components/NavBar/NavBar.vue'
import CanvasComponent from './components/Canvas/CanvasComponent.vue';

export default {
  name: 'App',
  data(){
    return {
      data: [{id: 1, type: "text", top: 0, left: 0, width: 30, height: 30, content: "This is awesome"}]
    }
  },
  components: {
    NavBar,
    CanvasComponent
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
