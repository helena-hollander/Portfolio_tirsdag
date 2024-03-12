<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header class="absolute w-screen z-10 pt-[1vh] pl-[1vw]">
      <nav class="grid grid-cols-6 h-[60px]">
        <RouterLink to="/about" class="bg-contain bg-no-repeat bg-[url('src/assets/about.png')] hover:bg-[url('src/assets/about_hover.png')] active:bg-[url('src/assets/about_click.png')] focus:bg-[url('src/assets/about_hover.png')]"></RouterLink>
        <RouterLink to="/contact" class="bg-contain bg-no-repeat bg-[url('src/assets/contact.png')] hover:bg-[url('src/assets/contact_hover.png')] active:bg-[url('src/assets/contact_click.png')] focus:bg-[url('src/assets/contact_hover.png')]"></RouterLink>
     </nav>
   
  </header>

  <RouterView></RouterView>
</template>

