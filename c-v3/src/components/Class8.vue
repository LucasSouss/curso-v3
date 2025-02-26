<template>
    <div class="dd">

        <input type="text" 
        v-model="name">
        
        {{ name }}

    </div>

    <div class="dd">
        <label for="houses">Hogwarts Houses</label>
        <select v-model="HH">
            <option value="">Choose</option>
            <option value="Griffindor">Griffindor</option>
            <option value="Ravenclaw">Ravenclaw</option>
            <option value="Hufflepuff">Hufflepuff</option>
            <option value="Slytherin">Slytherin</option>
        </select>
        {{ HH }}
    </div>
    <div class="dds">
        <label>Values</label>
        <input type="radio" v-model="vls" value="Yes"> Yes
        <input type="radio" v-model="vls" value="No"> No
        
    </div>
    {{ vls }}

    <div class="dds">
        <label for="">Contract</label> <br>
        <input type="checkbox" v-model="contract"> Sim, aceito os termos...
        {{ contract }}
    </div>

    <div>
        <label for="">Choose yours favorites colors</label> <br>
        <input type="checkbox" v-model="colors" value="Blue"> Blue
        <input type="checkbox" v-model="colors" value="Black"> black <br>
        {{ colors }} 
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            HH: '',
            vls: '',
            contract: false,
            colors: []
        }
    }
}
</script>

<style scoped>

.dd {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 100px;
    flex-direction: column;
}

.dds {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 100px;
    gap: 10px;
}
</style>