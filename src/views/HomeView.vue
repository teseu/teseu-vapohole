<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/TheCard.vue'
import List from '@/components/TheList.vue'

const items = ref([
  {
    id: 1,
    item: 'Item 1'
  },
  {
    id: 2,
    item: 'Item 2'
  }
])
</script>

<template>
  <main>
    <div class="flex">
      <img alt="Teseu logo" class="logo w-48 h-48" src="@/assets/teseu.png" />
      <h1 class="flex text-7xl w-full justify-center items-center pb-6">Página do Teseu</h1>
    </div>
    <div class="flex justify-between gap-4 mt-6">
      <Card class="w-full">
        <template #titulo>Interesses</template>
        <ul class="list-none">
          <List v-for="item in items" :key="item.id" :item="item.item">
          </List>
        </ul>
      </Card>
    </div>
  </main>
</template>
