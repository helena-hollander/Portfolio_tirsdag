<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import Image from '@/components/home_image.vue'
gsap.registerPlugin(ScrollTrigger);



export default {
  components: {
    Image
},
  mounted() {
    this.$nextTick(() => {
      let sections = gsap.utils.toArray(".project1view section");
      const length = sections.length - 1
      let scrollTween = gsap.to(sections, {
          xPercent: -100 * length,
          ease: "none",
          scrollTrigger: {
            trigger: ".project1view",
            pin: true,
            scrub: 0.1,
            end: "+=" + 1000 * length
          }
        });
    })
  }
}


</script>


<template>
  <!-- <div class="scroll h-screen">
   <div class="absolute">
    <img src="../../assets/Resting_web.jpg" class="grid h-[90vh] translate-x-[20vw] translate-y-[5vh]">
   </div>
  </div> -->
  <div class="flex flex-nowrap project1view">
    <section class="flex-none w-screen h-screen bg-red-500 relative">
      <Image image="src/assets/Lipstick_Lover_web.jpg" class="h-[65vh] absolute translate-x-[15vw] translate-y-[25vh]"></Image>
    </section>
    <section class="flex-none w-screen h-screen bg-yellow-500 relative">
      <Image image="src/assets/Mie_In_The_Sky_web.jpg" class="h-[45vh] absolute translate-x-[-5vw] translate-y-[40vh] "></Image>
    </section>
    <section class="flex-none w-screen h-screen bg-purple-500 relative">
      THREE
    </section>
  </div>
  </template>