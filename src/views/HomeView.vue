
<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Update ninja one</button>
    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }} - {{ nameTwo }}</p>
    <button @click="updateNinjaTwo">Update nina two</button>
  </div>
</template>

<script>
import { ref, reactive } from 'vue'
export default {
  name: 'Home',
  setup() {    
    const ninjaOne = ref({ name: 'Kyle', age: 16 })
    const ninjaTwo = reactive({ name: 'Kate', age: 13})

    const nameOne = ref('Kyle')
    const nameTwo = reactive('Kate')

    const updateNinjaOne = () => {
      ninjaOne.value.age = 52
    }
    const updateNinjaTwo = () => {
      ninjaTwo.age = 48
    }
    return { ninjaOne, updateNinjaOne, ninjaTwo, updateNinjaTwo, nameTwo }
  },
}
</script>