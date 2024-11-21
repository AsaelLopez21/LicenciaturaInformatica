<template>
  <div class="container" >
    <div class="row mt-2">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="col-12 text-center">
          <h2>Contador: {{counter}}</h2>  
        </div>
      </nav>
      <div class="col-12  d-flex justify-content-center gap-2">   
        <button class="btn btn-danger" @click = "handledDecrement" >
          -1
        </button>

        <button class="btn btn-success" @click = "handledReset">
          Reset
        </button>

        <button class="btn btn-primary" @click = "handledIncrement">
          +1
        </button>
      </div>

      <div class = "col-12">
        <hr>
        <h4>
          <button v-if="estatus" class="btn btn-primary" @click = "agregarNumero">
            Agregar
          </button>
        </h4>
        <h4>
          Elementos en la lista: {{listaNumeros.join(', ')}}
        </h4>


      </div>
    </div>
  </div>
</template>

<script setup>  
  import {ref} from "vue";

  const counter = ref(0); //?Recibe cualquier tipo de dato, es reactivo y de tipo number, es un objeto
  const estatus = ref(true);

  const handledIncrement = () =>{
    counter.value = counter.value + 1;
    verificar()
  }

  const handledDecrement = () =>{
    counter.value = counter.value - 1;
    verificar()
  }

  const handledReset = () =>{
    counter.value = counter.value-counter.value;
  }

  const listaNumeros = ref([]);

  const agregarNumero = (()=>{
    if(!listaNumeros.value.includes(counter.value)){
      listaNumeros.value.push(counter.value)
      verificar()
    }
    
  })

  const verificar = (()=>{
    if(listaNumeros.value.includes(counter.value)){
      estatus.value = false
    }else{
      estatus.value = true
    }
  })

  
</script>

<style>
  

</style>

