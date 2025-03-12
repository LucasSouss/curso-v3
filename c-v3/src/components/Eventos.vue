<template>

<button v-on:click="onClick">
    Enviar
</button>
<br>

<div @mouseover="onMouseOver" @mouseout="onMouseOut">
TA PASSANDO...
</div>

<form action="https://youtube.com.br/" @submit.capture="onSubmit"> 
    <button type="submit">
        Enviar
    </button>
</form>

<input type="text" @keyup="press">

</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        onClick() {
            console.log('Click')
        },
        onMouseOver() {
            console.log('Passou por cima')
        },
        onMouseOut() {
            console.log('Saiu')
        },
        onSubmit() {
            console.log('submit')
        },
        press() {
            console.log('digitando')
        }
    }
}



</script>

<style scoped>

</style>