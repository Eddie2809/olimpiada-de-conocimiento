<script>
  import Home from './components/Home.vue'
  import SubirPreguntas from './components/SubirPreguntas.vue'
  import Jugar from './components/Jugar.vue'

  export default{
    components: {
      Home,
      Jugar,
      SubirPreguntas
    },
    data(){
      return{
        route: 'Home',
        equipos: ["Lechugas","Tomates"],
        ronda: 1,
        preguntas: [
            {
                preguntaTexto: "Todo cuerpo persevera en su estado de reposo o movimiento uniforme y rectilíneo a no ser que sea obligado a cambiar su estado por fuerzas impresas sobre él",
                preguntaImagen: "",
                opciones: {
                    opcion1: "Segunda ley de Newton",
                    opcion2: "Tercera de la Termodinamica",
                    opcion3: "Tercera ley de Newton",
                    opcion4: "Ley de la Inercia",
                },
                respuesta: 4,
                categoria: "Ciencias Básicas",
                dificultad: "Fácil"
            },
            {
                preguntaTexto: "Es el número total de protones que tiene el átomo",
                preguntaImagen: "",
                opciones: {
                    opcion1: "Masa atómica",
                    opcion2: "Número de masa",
                    opcion3: "Número atómico",
                    opcion4: "Masa molecular",
                },
                respuesta: 3,
                categoria: "Ciencias Básicas",
                dificultad: "Fácil"
            },
            {
                preguntaTexto: "Son compuestos que poseen átomos de hidrógeno facilmente remplazables por átomos de metal",
                preguntaImagen: "",
                opciones: {
                    opcion1: "Hidróxidos",
                    opcion2: "Ácidos",
                    opcion3: "Bases",
                    opcion4: "Óxidos",
                },
                respuesta: 2,
                categoria: "Ciencias Básicas",
                dificultad: "Difícil"
            }
        ]
      }
    },
    methods: {
      changeRoute(newRoute){
        this.route = newRoute
      }
    }
  }
</script>

<template>
  <div class="App">
    <Home v-if="route === 'Home'" :changeRoute = "changeRoute"/>
    <Jugar :preguntas="this.preguntas" :equipos="this.equipos" :ronda="this.ronda" v-if="route === 'Jugar'"/>
    <SubirPreguntas v-if="route === 'SubirPreguntas'"/>
  </div>
 </template>