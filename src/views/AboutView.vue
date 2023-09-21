<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/TheCard.vue'
import List from '@/components/TheList.vue'

const items = ref([
  {
    id: 1,
    item: 'Vuejs 3'
  },
  {
    id: 2,
    item: 'Vite'
  },
  {
    id: 3,
    item: 'TailwindCSS'
  },
  {
    id: 4,
    item: 'Neovide com AstroVim'
  }
])
</script>

<template>
  <div class="flex flex-col">
    <div class="flex flex-col gap-4">
      <h1 class="text-3xl mb-4">Sobre esta página</h1>
      <Card>
        <template #titulo>Tecnologias</template>
        <ul class="text-xl">
          <List v-for="item in items" :key="item.id" :item="item.item">
          </List>
        </ul>
      </Card>
    </div>
    <div class="flex gap-4 mt-6">
      <h2 class="text-2xl mb-4">Alguns screenshots</h2>
    </div>
  </div>
</template>

<style></style>
