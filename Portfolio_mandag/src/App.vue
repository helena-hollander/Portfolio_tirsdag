<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
      <nav class="grid grid-cols-3 underline">
        <RouterLink to="/"><img src="./components/Logo.png" alt="Logo" class="w-[200px] pl-4"></RouterLink>
        <RouterLink to="/about">about</RouterLink>
        <RouterLink to="/contact">contact</RouterLink>
      </nav>
   
  </header>

  <RouterView></RouterView>
</template>

