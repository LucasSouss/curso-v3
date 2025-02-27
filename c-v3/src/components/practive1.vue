<template>
<h1>
    What's your Hogwarts House?
</h1>

<div class="checkbox-container">
    <label>Choose your values:</label>
    <div class="checkbox-wrapper">
      <input type="checkbox" v-model="vl" value="courage"> Courage
      <input type="checkbox" v-model="vl" value="nerve"> Nerve
      <input type="checkbox" v-model="vl" value="chivalry"> Chivalry
      <input type="checkbox" v-model="vl" value="brave"> Brave
      <input type="checkbox" v-model="vl" value="hard-work"> Hard Work
      <input type="checkbox" v-model="vl" value="patience"> Patience
      <input type="checkbox" v-model="vl" value="justice"> Justice
      <input type="checkbox" v-model="vl" value="loyalty"> Loyalty
      <input type="checkbox" v-model="vl" value="intelligence"> Intelligence
      <input type="checkbox" v-model="vl" value="learning"> Learning
      <input type="checkbox" v-model="vl" value="wisdom"> Wisdom
      <input type="checkbox" v-model="vl" value="wit"> Wit
      <input type="checkbox" v-model="vl" value="ambition"> Ambition
      <input type="checkbox" v-model="vl" value="cunning"> Cunning
      <input type="checkbox" v-model="vl" value="leadership"> Leadership
      <input type="checkbox" v-model="vl" value="resourcefulness"> Resourcefulness
    </div>
  </div>



<div class="checkbox-container">
    Your House: {{ sortedHouse }}
    <div class="imgL" v-if="sortedHouse === 'Gryffindor'">
        
    <img src="../assets/image/g-logo.png" alt="">
    
    </div>

    <div class="imgL" v-if="sortedHouse === 'Hufflepuff'">
        
        <img src="../assets/image/h-logo.png" alt="">
        
    </div>

    <div class="imgL" v-if="sortedHouse === 'Ravenclaw'">
        
        <img src="../assets/image/r-logo.png" alt="">
        
    </div>

    <div class="imgL" v-if="sortedHouse === 'Slytherin'">
        
        <img src="../assets/image/s-logo.png" alt="">
        
    </div>
</div>

</template>


<script>

export default {
    data() {
        return {
            vl: []
        }
    },
    computed: {
        sortedHouse() {
            const houses = {
                Gryffindor: ["courage", "nerve", "chivalry", "brave"],
                Hufflepuff: ["hard-work", "patience", "justice", "loyalty"],
                Ravenclaw: ["intelligence", "learning", "wisdom", "wit"],
                Slytherin: ["ambition", "cunning", "leadership", "resourcefulness"]
            }
            // Contador das casas. Conta o valor que cada casa receber
            const houseCounts = {Gryffindor: 0, Hunfflepuff: 0, Ravenclaw: 0, Slytherin: 0}

            this.vl.forEach(value => {
                for(const house in houses) {
                    if (houses[house].includes(value)) {
                        houseCounts[house]++
                    }
                }
            })

            const maxPoints = Math.max(...Object.values(houseCounts))

            if (maxPoints === 0) {
                return ''
            }

            return Object.keys(houseCounts).reduce((a,b) => (houseCounts[a] > houseCounts[b] ? a : b), "No house selected")
        }
    }
}

</script>

<style scoped>
h1 {
    text-align: center;
    padding: 15px;
}

.checkbox-container {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centraliza o texto */
    text-align: center;
    padding: 40px;
}

.checkbox-wrapper {
    display: flex;
    flex-wrap: wrap; /* Permite que os itens quebrem a linha */
    justify-content: center; /* Centraliza os c heckboxes */
    gap: 10px; /* Espaço entre os checkboxes */
    max-width: 500px; /* Define uma largura máxima para evitar espalhamento excessivo */
}
   
    

</style>