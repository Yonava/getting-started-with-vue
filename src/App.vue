<template>
  <div>
    <button @click="numOfCounters++">Add a Counter</button>
    <button @click="numOfCounters--">Remove a Counter</button>
    <div v-for="i in numOfCounters" :key="i">
      <Counter />
    </div>
  </div>
</template>

<script>
import Counter from './components/Counter.vue'
export default {
  components: { Counter },
  data() {
    return {
      numOfCounters: 3
    }
  }
}
</script>