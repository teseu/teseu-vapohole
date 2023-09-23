<script setup>
const props = defineProps({
 src: String,
 alt: String,
 addFClass: String,
 addIClass: String,
 addCClass: String,
 caption: String
});
</script> 

<template>
 <figure :class="addFClass">
  <img class="object-cover" :class="props.addIClass" :src="props.src" :alt="props.alt" />
  <figcaption :class="props.addCClass">{{ props.caption }}</figcaption>
 </figure>
</template>
<style scoped></style>
