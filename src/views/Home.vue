<template>
  <div class="home">
    Home
    <p>Name is {{ name }} and age is {{ age }}</p>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>

import {ref} from 'vue'

export default {
  // this is composition API. Normal JS inside
  // makes any props and transformed values, methods available in component
  name: 'Home',
  setup() {
    const name = ref('Wario')
    const age = ref(25)

    const handleClick = () => {
      name = 'Waluigi'

    }

    return {name, age, handleClick}
  }
}
</script>
