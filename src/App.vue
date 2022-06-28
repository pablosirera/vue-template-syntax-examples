<script setup>
import ExampleOptions from './components/ExampleOptions.vue'
import ExampleComposition from './components/ExampleComposition.vue'
import ExampleScript from './components/ExampleScript.vue'
</script>

<template>
  <main class="main">
    <ExampleOptions message="world" />
    <ExampleComposition message="world" />
    <ExampleScript message="world" />
  </main>
</template>

<style>
@import './assets/base.css';
#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
}
a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}
.example-components {
  border: 1px solid white;
  padding: 10px;
}
</style>
