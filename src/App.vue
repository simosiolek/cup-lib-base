<script setup>
  import cupButton  from './components/Button/Button.vue';
  import cupBadge  from './components/Badge/Badge.vue';
</script>

<template>
  <cupButton
    label="My Button"
  />&nbsp;
  <cupButton
    label="Click CTA"
    cta
  />
  <br /><br />
  <cupBadge
    label="Popular"
  />&nbsp;
  <cupBadge
    label="New"
    highlighted
  />
</template>
<!-- <style>
@import "assets/style.scss";
</style> -->