<template>
    <div class="row">
        <div class="col-5">
            <div class="card-body">
                <h4 class="card-title">{{ titulo }}</h4>
                <p class="card-text">{{ descripcionP }}</p>
                <!--!26-11-2024-->
                <a href="#"  class="btn btn-primary" @click="$emit('changeNameInCard',titulo)">Seleccionar</a>
            </div>
        </div>
        <div class="col-3">
            <img :src="imagen" class="card-img-top rounded-circle" alt="img_temp">
        </div>
    </div>
</template>

<script setup>
    defineProps({
        titulo: {
            type: String,
            default: 'Valor por default'
        },
        descripcionP: {
            type: String,  // Cambiado de typeof a type
            default: 'Descripcion default'  // Corrección en "defualt"
        },
        imagen: {
            type: String,
            required: true  // Cambiado de require a required
        }
    });
</script>

<style scoped>
/* Aquí puedes agregar estilos específicos para este componente */
</style>
