<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/TheCard.vue'
import List from '@/components/TheList.vue'
import Fedora from '@/components/icons/IconFedora.vue'
import Teseu from '@/assets/teseu.png'

const items = ref([
  {
    id: 1,
    item: 'Tecnologia em geral'
  },
  {
    id: 2,
    item: 'Linux, Fedora, Bash, Zsh, Shell Script'
  },
  {
    id: 3,
    item: 'Desenvolvimento Frontend'
  },
  {
    id: 4,
    item: 'Vuejs, Javascript, HTML, CSS, Tailwind'
  },
  {
    id: 5,
    item: 'Música em geral, coral, violão'
  },
  {
    id: 6,
    item: 'Literatura'
  },
  {
    id: 7,
    item: 'Cinema'
  }
])
</script>

<template>
  <main>
    <div class="flex">
      <img alt="Teseu logo" class="logo w-48 h-48" :src="Teseu" />
      <h1 class="flex text-7xl w-full justify-center items-center pb-6">Página do Teseu</h1>
    </div>
    <div class="flex justify-between gap-4 mt-6">
      <Card class="w-full">
        <template #titulo>Bio</template>
        <p class="text-lg mb-4">Pai, marido, geek, nerd, corista</p>
        <p class="text-lg mb-4">Usuário Fedora
          <Fedora class="w-5 inline" />, entusiasta de software Livre,
          membro do Time de Documentação do LibreOffice, membro da The
          Document Foundation - TDF
        </p>
        <p class="text-lg mb-4">Servidor publico federal, nascido e criado em
          Brasília</p>
        <p class="text-lg">Fã de Star Wars, O Senhor dos Anéis, Matrix, Duna,
          FullMetal Alchemist, Star Trek, Quadrinhos (Marvel, DC, Dark Horse,
          Vertigo)</p>
      </Card>
      <Card class="w-full">
        <template #titulo>Interesses</template>
        <ul class="list-none">
          <List v-for="item in items" :key="item.id" :item="item.item">
          </List>
        </ul>
      </Card>
    </div>
    <div class="flex text-xl mt-6">Apenas um pouco sobre mim e meus interesses</div>
  </main>
</template>
