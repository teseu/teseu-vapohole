<script setup>
import { PhCheckFat } from '@phosphor-icons/vue'
const props = defineProps(['item']);
</script>

<template>
  <li class="flex items-center mb-2">
    <PhCheckFat class="mr-4" color="#059669" :size="32" weight="duotone" />
    <span class="text-lg">{{ item }}</span>
  </li>
</template>
