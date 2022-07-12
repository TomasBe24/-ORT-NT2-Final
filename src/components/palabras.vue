<template>

  <section class="src-components-palabras">
    <br>
    Palabras: {{getPalabras}}
  </section>

</template>

<script>

  export default  {
    name: 'src-components-palabras',
    props: ['texto'],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {
      getPalabras(){
        let arrayPalabras = this.texto.trim().split(' ')
        let cantPalabras = arrayPalabras.length

        return cantPalabras
      }
    }
}


</script>

<style scoped>
  
</style>
