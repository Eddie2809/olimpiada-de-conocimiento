<script>
    export default{
        props: ['opciones','preguntaActiva']
    }
</script>

<template>
    <div class="Opciones">
        <div class="opcion card"><p>A) <span>{{opciones.opcion1}}</span></p></div>
        <div class="opcion card"><p>B) <span>{{opciones.opcion2}}</span></p></div>
        <div class="opcion card"><p>C) <span>{{opciones.opcion3}}</span></p></div>
        <div class="opcion card"><p>D) <span>{{opciones.opcion4}}</span></p></div>
    </div>
</template>