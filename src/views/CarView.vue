<script setup>
  import {useRoute,useRouter,RouterView} from "vue-router"
  import cars from '../data/cars.json'

  const route = useRoute()
  const router = useRouter()

  const carId = parseInt(route.params.id)

  const car = cars.find(c => c.id === carId)

  const showContact =() =>{
    if(carId === 5) return;
    return router.push(`/cars/${carId}/contact`)
  }

</script>

<template>
    <main>
    <div v-if="car">
        
        <h1>{{ car.name }}'s Details</h1>
        <p>{{ car.name }}</p>
        <p>{{ car.price }}</p>
        <p>{{ car.year }}</p>
        <!-- <button @click="router.push(`/cars/${carId}/contact`)">To Contact</button> -->
        <button @click="showContact()">To Contact</button>
        <RouterView/>
    </div>
    <div v-else>
        <h1>Car Not Found!</h1>
    </div>
</main>
</template>