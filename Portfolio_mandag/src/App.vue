<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header class="absolute w-screen z-10 pt-[1vh] pl-[1vw]">
      <nav class="grid grid-cols-3 h-[60px]">
        <RouterLink to="/" class="bg-contain bg-no-repeat bg-[url('src/assets/gallery.png')] hover:bg-[url('src/assets/gallery_hover.png')] active:bg-[url('src/assets/gallery_click.png')] focus:bg-[url('src/assets/gallery_hover.png')] bg-center"></RouterLink>
        <RouterLink to="/about" class="bg-contain bg-no-repeat bg-[url('src/assets/about.png')] hover:bg-[url('src/assets/about_hover.png')] active:bg-[url('src/assets/about_click.png')] focus:bg-[url('src/assets/about_hover.png')] bg-center"></RouterLink>
        <RouterLink to="/contact" class="bg-contain bg-no-repeat bg-[url('src/assets/contact.png')] hover:bg-[url('src/assets/contact_hover.png')] active:bg-[url('src/assets/contact_click.png')] focus:bg-[url('src/assets/contact_hover.png')] bg-center"></RouterLink>
     </nav>
  </header>
  
  <RouterView></RouterView>
</template>

