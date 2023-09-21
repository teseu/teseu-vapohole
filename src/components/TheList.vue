<script setup>
import { PhCheckFat } from '@phosphor-icons/vue'
const props = defineProps(['item']);
</script>

<template>
  <li class="flex items-center">
    <PhCheckFat class="mr-4" color="#059669" :size="32" weight="fill" />
    <span class="text-lg">{{ item }}</span>
  </li>
</template>
