<template>
    <div>
        <p>Nome: {{ fName }}</p>
        <p>Sobrenome: {{ lName }}</p>
    </div>
</template>


<script>


export default {


    
    data() {
        return {
            fName: 'José',
            lName: 'Bragantino'
        }
    }
}

</script>


<style scoped>

</style>