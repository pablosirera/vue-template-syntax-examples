<template>
  <section class="example-components">
    <h2>Example with Options API</h2>
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

<script>
export default {
  name: 'ExampleOptions',
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      items: ['Item1', 'Item2', 'Item3'],
    }
  },
  computed: {
    fullMessage() {
      return `Hello ${this.message}`
    },
  },
  mounted() {
    console.log('Hello example')
  },
  methods: {
    sayHi() {
      alert('Hi Options API!')
    },
  },
}
</script>
