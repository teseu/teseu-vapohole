<script setup>
import Card from '@/components/ui/TheCard.vue'
 import Title from '@/components/ui/TheTitle.vue'
</script>

<template>
  <div class="flex flex-col">
    <div class="flex flex-col gap-4">
      <Title>
        <template #titulo>Dicas</template>
      </Title>
      <Card>
        <template #titulo>Tecnologias</template>
        <h2 class="text-3xl">Em breve</h2>
      </Card>
    </div>
    <div class="flex flex-col gap-4 mt-6">
      <h2 class="text-2xl mb-4"></h2>
      <div class="text-xl mt-4"></div>
    </div>
  </div>
</template>
<style scoped>
 
</style>