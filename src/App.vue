<script setup>
// import  {RouterView} from 'vue-router'
import {ref} from "vue"
import Nav from "./components/Nav.vue"
import ContactView from './views/ContactView.vue';

// const btnclick = ref("")

</script>


<template>
  <div>
    <!-- {{ btnclick }} -->
    <!-- <HomeView/> -->
    <!-- <button @click="btnclick = 'hello'">Click Me</button> -->
    <Nav/>
    <RouterView/>
    
  </div>
  
</template>