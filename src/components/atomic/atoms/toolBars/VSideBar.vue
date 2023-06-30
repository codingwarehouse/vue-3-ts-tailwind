<script setup lang="ts">
import { useRouter } from 'vue-router'
import type { SideBarItemInterface } from '@/model/atomic/SideBarItemInterface'

// declare all props
defineProps({
  items: {
    type: Array as () => SideBarItemInterface[],
    default: () => []
  }
})

// declare all const && variables
const router = useRouter()

// methods (callback)
const redirect = (route: string) => {
  router.push(route)
}
</script>

<template>
  <div id="toolbar-sidebar">
    <div v-for="(el, key) in items" :key="key" @click="redirect(el.route)">
      <span>{{ el.icon }}</span>
      <span class="text-lg text-purple-900">{{ el.text }}</span>
    </div>
  </div>
</template>

<style scoped></style>
