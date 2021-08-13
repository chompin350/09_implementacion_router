<template>
    <div>
       <h1 v-text="tituloEntrada"></h1>
       <router-link :to="{name : 'articulo'}">Ver post</router-link>
        <!-- esta linea debe ir si ponermos un componente dependiente de otro -->
        <router-view></router-view> 
        <hr>
    </div>
</template>

<script>
export default {
     computed: { 
        tituloEntrada(){
            return `Este es el post N° ${this.$route.params.registro} del Blog` }
    }, 
}
</script>