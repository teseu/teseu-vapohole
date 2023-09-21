<script setup>
 
</script>

<template>
 <div class="rounded-lg border border-emerald-950 shadow-md flex flex-col">

    <div class="text-xl font-semibold bg-gradient-to-b from-emerald-800 to-emerald-900 text-emerald-50 rounded-t-lg px-6 py-2">
    <h2>
      <slot name="titulo"></slot>
    </h2>
</div>


    <div class="text-emerald-50 p-8">

    <slot></slot>

    </div>
 </div>
</template>
<style scoped>
 
</style>