<template>
    <h1>
        Are you wish to learn a new language?
    </h1>

    <div class="sele">
        <label for="opn">Click here:</label>
        <select v-model="selected">
            <option value="">selection...</option>
            <option value="op1">NO</option>
            <option value="op2">YES</option>
        </select>
    </div>

    <div class="option1" v-if="selected === 'op1'">
        <img src="../assets/image/hommer.gif" alt="hommer simpson">

    </div>

    <div class="option2" v-if="selected === 'op2'">
        <h2>GREAT CHOICE!</h2>
        <h3>There is the best way</h3>
        <h3>Watch this video</h3>
        <iframe width="560" height="315" src="https://www.youtube.com/embed/uWQYqcFX8JE?si=LZSWyKH-voJb1knZ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </div>
</template>

<script>

export default {
    data() {
        return {
            selected:""
        }
    }
}

</script>

<style scoped>

h1 {
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    padding: 15px;

}

.sele {
    text-align: center;
}

.option1 {
    padding: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
   
}

.option2 {
    padding: 25px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 10px;
}
</style>