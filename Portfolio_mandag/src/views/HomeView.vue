<script>
import Logo from '../components/bg_logo_com.vue'
import Image from '../components/home_image.vue'

export default {
    components: {
        Logo,Image,
    },
}
</script>

<template>
    <div class="px-[1vw] h-screen grid self-center absolute z-10 pointer-events-none">
        <Logo></Logo>
    </div>
    <div class="">
        <RouterLink to="/project1">
            <Image image="src/assets/Resting_web.jpg" class="pt-[0.5vw] h-[35vh] absolute translate-y-[10vh]"></Image>
        </RouterLink>
        <Image image="src/assets/imaginary_friends_scaled.jpg" class="h-[20vh] absolute translate-x-[15vw] translate-y-[30vh]"></Image>
        <Image image="src/assets/Mie_In_The_Sky_web.jpg" class="h-[45vh] absolute translate-x-[60vw] translate-y-[40vh] "></Image>
    </div>

</template>
