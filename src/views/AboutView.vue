<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/TheCard.vue'
import List from '@/components/TheList.vue'
import Title from '@/components/ui/TheTitle.vue'
import Imagem from '@/components/ui/PlaceImage.vue'
import Li from '@/assets/img/li.png'
import Tmux from '@/assets/img/tmux.png'
import Neovide from '@/assets/img/neovide.png'

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
  <div class="flex flex-col mb-8">
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
      <Card class="mb-8">
        <template #titulo>Terminal</template>
        <div class="flex justify-center gap-6">
          <div class="max-w-max">
            <h2 class="text-3xl mb-4">Tmux customizado</h2>
            <Imagem
            class="mb-8"
            addFClass="w-full hover:scale-150 transition-all duration-300"
            addIClass="rounded-t-lg mx-auto"
            addCClass="bg-neutral-950 px-2 py-1 rounded-b-lg"
            :src="Tmux" 
            alt="terminal rodando tmux customizado"
            caption="Terminal rodando tmux customizado"
            />
          </div>
          <div class="max-w-max">
            <h2 class="text-3xl mb-4">Comando li</h2>
            <Imagem
            class="mb-8"
            addFClass="w-full hover:scale-150 transition-all duration-300"
            addIClass="rounded-t-lg mx-auto"
            addCClass="bg-neutral-950 px-2 py-1 rounded-b-lg"
            :src="Li" 
            alt="terminal rodando comando li - alias de 'exa - lah--icons'"
            caption="Terminal rodando comando li - alias de 'exa - lah--icons'"
            />
          </div>
        </div>
      </Card>
      <Card>
        <template #titulo>Neovide com AstroVim</template>
        <h2 class="text-3xl mb-4">Customizações do Neovide</h2>
        <Imagem
            class="mb-8"
            addFClass="w-full hover:scale-105 transition-all duration-300"
            addIClass="rounded-t-lg mx-auto"
            addCClass="bg-neutral-950 px-2 py-1 rounded-b-lg"
            :src="Neovide" 
            alt="Neovide com customizações do AstroVim"
            caption="Neovide com customizações do AstroVim"
            />
      </Card>
    </div>
  </div>
</template>

<style></style>
