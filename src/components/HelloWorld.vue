<template>
  <div>

    Color: <input type="text" v-model="color">
    Fondo: <input type="text" v-model="fondo">
    Size: <input type="text" v-model="size">
    <hr>

    Texto: <input type="text" v-model="texto"
    :style="getStyle">

    {{ texto }}

    <palabras v-show="texto " :texto="texto"  />

    <table>
      <tr>
        <th>Pregunta</th>
        <th>Respuesta</th>
      </tr>
      <tr>
        <td>1</td>
        <td>B</td>
      </tr>
      <tr>
        <td>2</td>
        <td>C</td>
      </tr>
      <tr>
        <td>3</td>
        <td>B</td>
      </tr>
      <tr>
        <td>4</td>
        <td>D</td>
      </tr>
      <tr>
        <td>5</td>
        <td>D</td>
      </tr>
    </table> 

  </div>
   
</template>

<script>

import palabras from './palabras.vue'
export default {
  name: 'HelloWorld',
  components: {
    palabras
  },
  props: {
    
  },
  data() {
    return{
      texto : "",
      color : '',
      fondo : '',
      size : ''
    }
  },
  methods: {
  },
  computed: {
    getStyle(){
      return { 
        'color': this.color,
        'background-color': this.fondo,
        'font-size': this.size
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
