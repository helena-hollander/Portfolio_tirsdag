<script>
import Logo from '../components/bg_logo_com.vue'

export default {
    components: {
        Logo,
    },
}
</script>

<template>
    <div class="px-[1vw] h-screen grid absolute">
        <Logo></Logo>
    </div>
    <div class="absolute end-0 bottom-0">
        <img src="../assets/headshot_web.png" class="grayscale hover:grayscale-0">
    </div>

</template>
