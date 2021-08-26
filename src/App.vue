<template>
  <div>
    <h1>Crear una tarea nueva</h1>
    
    <h4>Tarea</h4>
    <input type="text" placeholder="Ingresa una nueva tarea" v-model="nuevaTarea">
    <button @click="agregarNuevaTarea()">Crear</button>

    <h2>Lista</h2>
    <ul>
      <li v-for="(tarea, $index) in tareas" :key="$index">{{$index}}:  {{tarea}}</li>
    </ul>
    
    
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    nuevaTarea: "",
    tareas: [],
  }),
  methods : {
    agregarNuevaTarea(){
        this.tareas.push(this.nuevaTarea)
        this.nuevaTarea = ""
    }
  }
};
</script>


<style scoped>
/* scoped, estilo para componente */
div {
  font-family: sans-serif;
  }
</style>
