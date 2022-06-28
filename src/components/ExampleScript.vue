<template>
  <section class="example-components">
    <h2>Example with Composition API (Script Setup)</h2>
    <p>Message from prop: {{ message }}</p>
    <ul>
      <li v-for="item in items" :key="item">
        {{ item }}
      </li>
    </ul>
    <p>Full message: {{ fullMessage }}</p>
    <button @click="sayHi()">Say hi</button>
  </section>
</template>

<script setup>
import { computed, onMounted, ref } from 'vue'

const props = defineProps({
  message: {
    type: String,
    required: true,
  },
})

const items = ref(['Item1', 'Item2', 'Item3'])

const fullMessage = computed(() => {
  return `Hello ${props.message}`
})

onMounted(() => {
  console.log('Hello example')
})

const sayHi = () => {
  alert('Hi Composition API (Script setup)!')
}
</script>
