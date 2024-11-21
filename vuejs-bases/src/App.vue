<!--!Componentes principal o padre, los nombres de los componentes se escriben con pascal case-->
<template> <!--!Se va a renderizar en nuestro proyecto -->
  <div class="container" >
    <!-- <h5>HOla</h5>
    <h3>Tamaño de la letra"{{nombre}}" es {{ nombre.length }}</h3> <!--! ESTA variable esta abajo en script setup, se llama interpolacion-->
    
    <!--*  v-bind: modificar atributos de las etiquetas
    <p v-bind:style="style">Azulito</p> <!--? El v-bind ya trae las llaves estas {{}}
    <p v-bind:style="`color:${colores[1]}`">Azulito</p>
    <p :style="`color:${colores[0]}`">Azulito</p> <!--?Los dos puntos es para ahorra v-bind-->
    
    <!--INFO<!--!EXPRESIONES
    {{isValid ?  'Soy valido':'No soy valido'}} -->

  <!--INFO!Uso del v-if-->
  <!-- <div v-if="estatus"  class="card" style="width: 18rem;">
    <img src="..." class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title">Datos Personales</h5>
      <!-- <p class="card-text">Asael Lopez</p> -->
    <!--</div>
    <!--<ul class="list-group list-group-flush">
      <li class="list-group-item">Nombre: Asael </li>
      <li class="list-group-item">Apellido: Lopez</li>
      <li class="list-group-item">Edad: 19</li>
    </ul>
    <div class="card-body ">
      <h4>Status: {{ estatus ? 'Activo':'Inactivo' }}</h4>
      <a href="#" class="card-link">Card link</a>
      <a href="#" class="card-link">Another link</a>
    </div>
    
  </div>
  
  <h2 v-if="estatus" class="text-succes">condicion verdadera</h2>
  <h2 v-if="!estatus" class="text-danger">condicion falsa</h2> 
  </div>

  <div class="container">
    <h2 v-if="estatus==true" class="text-success">condicion verdadera</h2>
    <h3 v-else-if="estatus == false" class="text-danger">Condicion falsa</h3>
    <h3 v-else class="text-succes">Es NULL</h3>
  </div> -->

  <!--!Display-->
    <!-- <ul><!--INFO usando vfor
      <li v-for="(fruta,index) in frutas":key="fruta">
        Fruta: {{index}} {{ fruta }}
      </li>
    </ul>

    <div><!--INFO vfor para objetos
      <b>Imprimiendo un objeto</b>
      <p>Datos</p>
      <h2 v-for="(algo,key) in persona":key="algo">
        {{key}} = {{ algo }}
      </h2>
    </div> -->

    <!--!___________________13-11-2024______________ -->
    <!-- <ul class="list-group">
      <template v-for="p in productos":key="p.id"><!--?INFO usando template para renderizar solo lo que cumple la condicion 
        <li v-if="p.stock > 400" class="list-group-item">
          {{ p.nombre }} -> {{ p.precio }}
        </li>
      </template>
    </ul> -->
      <!--TODO manejo de eventos-->
      <!--? usando v-on o el arroba -->
    <!-- <div class="row mt-2">
      <div class="col-2">
        <button @:click="handle" class="btn btn-outline-primary">BOTON</button>
      </div>
      <div class="col">
      
      </div>
      <hr>
      <h3>HOla</h3>
    </div> -->
    <!--!___________________14,19-11-2024______________ -->
    <!--TODO REACTIVIDAD-->
    
    <!--<div class="row mt-2">-->
      
      <!--!<h4 v-if="mayorCero" class="text-succes">Contador: {{ counter }}</h4>  ya accede por defecto al punto value-->
      
      <!-- <div class="col-2">
        <!--?valores computados, getStyle es propiedad usando computed, getStyle() es una funcion
        <h2 :class="getStyle">Contador: {{ counter }}</h2>
        <button class="btn btn-primary" @click="handledIncrement">
          +1
        </button>

        <button class="btn btn-primary" @click="handledReset">
          Reset
        </button>

        <button class="btn btn-primary" @click="handledDecrement">
          -1
        </button>
      </div>
    </div> -->
    <h1 class="text-primary">App</h1>
    <hr>
    <CounterButton></CounterButton>

  </div>
  

</template>

<script setup>  
  // const nombre = "Vuejs 3" //TODO:Aqui esta la variable que usamos en HTML
  // const colores = ['Red','Blue','Yellow']
  // const style = `color: ${colores[2]}`

  // //ERROREXPRESIONES
  // const isValid = false;
  //
  // //___________________12-11-2024______________
  // const estatus = true; //activo - inactivo //ERROR para probar v-if v-else
  
  // const frutas = ['Platano','Manzana','Naranja','Uva'] //ERROR v-for

  // const persona = {
  //   Nombre: "Asael",
  //   Apellidos: "Lopez",
  //   Edad: 19
  // }
  //___________________13-11-2024______________
  //INFO para probar template y v-if
  // const productos = [
  //   {
  //     id: 0,
  //     nombre: 'zapatos',
  //     precio: 100, 
  //     descripcion:'de calidad',
  //     stock:4
  //   },
  //   {
  //     id: 1,
  //     nombre: 'revista',
  //     precio: 10, 
  //     descripcion:'de noticias',
  //     stock:400
  //   },
  //   {
  //     id: 2,
  //     nombre: 'mariscos',
  //     precio: 80, 
  //     descripcion:'de la costa',
  //     stock:500
  //   },
  // ]

  //TODO: manejo de eventos
  // const styleH = 'container-fluid text-center text-primary'

  // const mensaje = 'Hola Mundo'
  // const handle = () =>{
  //   console.log('Diste un click');
  // }
  //!ERROR___________________14-11-2024______________ -->

  //TODO: REACTIVIDAD
  
  // import {ref} from "vue";

  // const counter = ref(0); //?Recibe cualquier tipo de dato, es reactivo y de tipo number, es un objeto
  
  // const handledIncrement = () =>{
  //   counter.value = counter.value + 1;
  // }

  // const handledDecrement = () =>{
  //   counter.value = counter.value - 1;
  // }

  // const handledReset = () =>{
  //   counter.value = counter.value-counter.value;
  // }

  
  // const estatus = true

  // if(counter.value>0){
  //   mayorCero = true
  // }else{
  //   mayorCero = false
  // }

  //<!--!___________________19-11-2024______________ -->
  //<!--!valores computados>
  // import {ref,computed} from "vue";

  // const counter = ref(0); //?Recibe cualquier tipo de dato, es reactivo y de tipo number, es un objeto

  // const handledIncrement = () =>{
  //   counter.value = counter.value + 1;
  // }

  // const handledDecrement = () =>{
  //   counter.value = counter.value - 1;
  // }

  // const handledReset = () =>{
  //   counter.value = counter.value-counter.value;
  // }

  // //TODO: Variable conputada
  // const getStyle = computed(()=>{
  //   if(counter.value === 0)return 'text-success'
  
  //   if(counter.value > 0)return 'text-primary'
    
  //   if(counter.value < 0) return 'text-danger'     
  // })

  //<!--!Importar componente para ir al otro archivo vue-->
  import CounterButton from "./components/CounterButton.vue";

</script>

























<!-- <script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div>
    <a href="https://vite.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style> -->
