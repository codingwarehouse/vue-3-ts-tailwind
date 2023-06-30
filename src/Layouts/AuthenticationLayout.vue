<script setup lang="ts">
import { useRoute } from 'vue-router'
import { computed } from 'vue'
import { Layouts } from '@/enums/Layouts'

const route = useRoute()
const layout = computed(() => route.meta.layout ?? Layouts.Default)
</script>

<template>
  <div>
    <h1>{{ layout }}</h1>
  </div>

  <div>
    <router-view />
  </div>
</template>
