<template>
  <div :class="classes">{{ label }}</div>
</template>

<script setup>
// import './button.css';
import { defineProps, computed } from 'vue'

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  highlighted: {
    type: Boolean,
    default: false,
  }
})

const classes = computed(() => ({
  'badge': true,
  'badge--highlighted': props.highlighted
}))
</script>

<style lang="scss">
.badge {
  font-size: 0.75rem;
  border-radius: 0.25em;
  background-color: var(--badge-bg);
  color: var(--badge-color);
  display: inline-block;
  line-height: 1;
  padding: 0.25rem 0.375rem;
  
  &--highlighted {
    background-color: var(--badge-highlighted-bg);
  }
}
</style>