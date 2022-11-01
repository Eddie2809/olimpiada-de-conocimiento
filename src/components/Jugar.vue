<script>
    export default{
        data(){

        },
        props: ['match'],
        methods: {
            async fetchPost(route,body){
                fetch()
            }
        }
    }
</script>

<template>
    <div class="Game">
        <div class="welcomeMsg" @keypress.enter="changeInnerIf('teams')">
            <h2 class="subtitle">Bienvenido a la</h2>
            <h1 class="title">Olimpiada de Conocimiento</h1>
        </div>
    </div>
</template>