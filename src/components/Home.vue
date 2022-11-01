<script>
    export default{
        data(){
            return{

            }
        },
        props: ['changeRoute']
    }
</script>

<template>
    <div class="Home">
        <div class="menu" >
            <button class="main-btn" @click="this.changeRoute(1)">Jugar</button>
            <button>Subir preguntas</button>
            <button>Ver preguntas</button>
            <button>Configuraciones</button>
        </div>
    </div>
    
</template>