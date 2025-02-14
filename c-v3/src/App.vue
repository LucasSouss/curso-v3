
<template>

 
    <TheHeader v-if="showHeader"/>

    <div v-show="showName">
      Nome: {{ firstname }} <br>
      Sobrenome: {{ lastname }}
    </div>

    <div v-if="accesslevel === 'admin'">Admin</div>
    <div v-else-if="accesslevel === 'marketing'">Marketing</div>
    <div v-else>Use</div>
  
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader
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
