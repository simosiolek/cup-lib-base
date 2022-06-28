<template>
  <button type="button" :class="classes" @click="onClick" >{{ label }}</button>
</template>

<script setup>
// import './button.css';
import { defineProps, computed } from 'vue'

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  cta: {
    type: Boolean,
    default: false,
  }
})

const classes = computed(() => ({
  'btn': true,
  'btn--cta': props.cta
}))
</script>

<style lang="scss">
.btn {
  font-weight: 700;
  border: 0;
  border-radius: 0.5em;
  background-color: var(--button-bg);
  color: white;
  cursor: pointer;
  display: inline-block;
  line-height: 1;
  padding: 0.75rem 1rem;
  transition: all linear 0.15s;

  &:hover {
    background-color: var(--button-bg-hover); 
  }
  
  &--cta {
    background-color: var(--button-cta-bg);

    &:hover {
      background-color: var(--button-cta-bg-hover); 
    }
  }
}
</style>