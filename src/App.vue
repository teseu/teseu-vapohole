<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    <div class="wrapper">
      <nav class="w-[80vw] mx-auto flex justify-start gap-4 py-4 mb-4 relative">
        <RouterLink class="link" to="/">Home</RouterLink>
        <RouterLink class="link" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView class="w-[80vw] mx-auto" />
</template>

<style scoped>
.link {
  @apply w-20 text-center text-emerald-300 hover:text-emerald-600 before:absolute before:ml-[-1.1rem] before:w-0 before:h-[2px] before:bottom-3 before:bg-transparent hover:before:w-20 hover:before:bg-emerald-800 transition-all before:transition-all duration-300 before:duration-300;
}
.link.router-link-active {
  --tw-text-opacity: 1;
  color: rgb(248 250 252 / var(--tw-text-opacity));
}
</style>
