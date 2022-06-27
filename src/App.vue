<script setup>
  import cupButton  from './components/Button/cupButton.vue';
</script>

<template>
    <cupButton
    label="My Button"
  />
  <cupButton
    label="Click CTA"
    cta
  />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
