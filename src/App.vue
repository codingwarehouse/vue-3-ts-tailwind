<script setup lang="ts">
import { useRoute } from 'vue-router'
import { computed } from 'vue'
import { Layouts } from '@/enums/Layouts'
import DefaultLayout from '@/Layouts/DefaultLayout.vue'
import AuthenticationLayout from '@/Layouts/AuthenticationLayout.vue'

const route = useRoute()

const isDefaultLayout = computed(
  () => (route.meta.layout || route.meta.layout === Layouts.Default) ?? true
)
const isAuthenticationLayout = computed(() => route.meta.layout === Layouts.Authentication)
</script>

<template>
  <div id="display-layouts">
    <AuthenticationLayout v-if="isAuthenticationLayout"></AuthenticationLayout>
    <DefaultLayout v-else-if="isDefaultLayout"></DefaultLayout>
    <div v-else>You should not be here</div>
  </div>
</template>
