<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  setup() {
    console.log('setup')

    let name = 'Kyle'
    let age = 16

    const handleClick = () => {
      console.log('You clicked me')
    }
    
    return { name, age, handleClick}
  }
}
</script>
