<script setup lang="ts">
defineProps({
  color: String,
  disabled: Boolean,
  outlined: Boolean,
  rounded: Boolean,
  elevation: Number
})
</script>

<template>
  <button
    v-if="outlined"
    type="button"
    :class="`btn btn-outline-${color} ${!disabled ?? 'btn-disabled'}`"
  >
    <slot></slot>
  </button>

  <button v-else type="button" :class="`btn btn-${color} ${!disabled ?? 'btn-disabled'}`">
    <slot></slot>
  </button>
</template>

<style scoped>
@import '../../../../assets/Button/Button.css';
</style>
