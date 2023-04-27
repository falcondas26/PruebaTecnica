<template>
  <div id="app">
        <bienvenida @mostrarDiv="RecibirEstado" />
        <Explicaciones v-show="vista" @mostrarDiv="RecibirEstado2"/>
        <draganddrop v-show="vista2"/>
  </div>
</template>

<script>
import bienvenida from "@/components/Bienvenida.vue"
import Explicaciones from "./components/Explicaciones.vue";
import draganddrop from "./components/DragDrop.vue"
export default {
  name: 'App',
  data(){
    return{
      vista: false,
      vista2: false
    }
  },
  components: {
    bienvenida,
    Explicaciones,
    draganddrop,
  },
  methods:{
    RecibirEstado(e){
      setTimeout(() => {
            this.vista=e   
      }, 1000);
    },
    RecibirEstado2(e){
      setTimeout(() => {
            this.vista2=e   
      }, 1000);
    }
  }
  
  
}
</script>

<style>


.fade-enter-active, .fade-leave-active {
  transition: opacity 1s
}
.fade-enter, .fade-leave-to  {
  opacity: 0
}


</style>
