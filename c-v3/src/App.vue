
<template>

    <!-- <Class8/> -->
    <!-- <TheHeader v-if="showHeader"/>  -->
    <!-- <Test02/> -->
    <!-- <Practive1/> -->
    <Eventos/>
    
  
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'
import Test02 from './components/Test02.vue'
import Class8 from './components/Class8.vue'
// import Practive1 from './components/practive1.vue';
import Eventos from './components/Eventos.vue';


export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader,
    Test02,
    Class8,
    // Practive1,
    Eventos
  },
  data() {
    return {
      showHeader: true,
      firstname: 'Jon Snow',
      lastname: 'Targaryan',
      showName: true,
      accesslevel: 'admin'
    }
  }
}
</script>


<style scoped>
tab {
  background-color: white;
  color: black;
}
</style>
