<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/TheCard.vue'
import List from '@/components/TheList.vue'
import Title from '@/components/ui/TheTitle.vue'

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
      <Title>
        <template #titulo>Sobre essa página</template>
      </Title>
      <Card>
        <template #titulo>Tecnologias</template>
        <ul class="text-xl">
          <List v-for="item in items" :key="item.id" :item="item.item">
          </List>
        </ul>
      </Card>
    </div>
    <div class="flex flex-col gap-4 mt-6">
      <h2 class="text-2xl mb-4">Alguns screenshots</h2>
      <div class="text-xl mt-4">Em breve</div>
    </div>
  </div>
</template>

<style></style>
