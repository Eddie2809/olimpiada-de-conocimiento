<script>
    import Opciones from './Opciones.vue'
    import Pregunta from './Pregunta.vue'
    import Respuesta from './Respuesta.vue'
    import Puntajes from './Puntajes.vue'
    import Tiempo from './Tiempo.vue'

    export default{
        components: {
            Opciones,
            Pregunta,
            Respuesta,
            Puntajes,
            Tiempo
        },
        data(){
            return{
                estadoTemporizador: 'preparado',
                preguntaActiva: 2,
                respuesta: 'incorrecto',
                respondido: false
            }
        },
        props: ['preguntas','equipos','puntajes']
    }
</script>

<template>
    <div v-if="!this.respondido" class="interfazPregunta">
        <Puntajes :puntajes="puntajes" :equipos="equipos" />
        <div class="int-preg-mid">
            <Pregunta :preguntaActiva="this.preguntaActiva" :preguntas="preguntas" />
            <Tiempo :estadoTemporizador="this.estadoTemporizador"/>
        </div>
        <Opciones :opciones="preguntas[preguntaActiva].opciones" :preguntaActiva="this.preguntaActiva" />
    </div>
    <div v-if="this.respondido" class="respuesta">
        <div v-if="this.respuesta === 'correcto'" class="correcto">
            <p>Pregunta: <span></span></p>
            <p>Respuesta: <span></span></p>
        </div>
        <div v-if="this.respuesta === 'incorrecto'" class="incorrecto">Respuesta incorrecta</div>
    </div>
</template>