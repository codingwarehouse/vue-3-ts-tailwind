<script setup lang="ts">
import VButton from '@/components/atomic/atoms/buttons/VButton.vue'
import IconDocumentation from '@/components/icons/IconDocumentation.vue'

defineProps<{
  msg: string
}>()
</script>

<template>
  <div>
    <h1 class="font-sans text-gray-500 text-5xl underline decoration-pink-600">i am alive</h1>
  </div>

  <div>
    <v-button disabled>something <IconDocumentation class="pl-2" /></v-button>
  </div>

  <div>
    <div v-for="i in 3" :key="i">
      <button type="button" :class="`rounded-full bg-amber-${i ? i * 100 : 100}`">
        button {{ i }}
      </button>
      <button type="button" class="rounded-full bg-amber-200">button {{ i }}</button>
    </div>
  </div>

  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>. What's next?
    </h3>
  </div>
</template>
