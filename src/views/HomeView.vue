<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
    <button @click="age++">Add 1 to Age</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'

export default {
  name: 'HomeView',
  setup() {
    // const p = ref(null)

    const name = ref('Kyle')
    const age = ref(16)


    const handleClick = () => {
      name.value = 'Kate'
      age.value = 13
    }
    
    return { name, age, handleClick}
  },
  data() {
    return {
      score: 5
    }
  }
}
</script>
