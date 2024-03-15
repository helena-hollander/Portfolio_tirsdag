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
            scrub: true,
            end: "+=" + 1000 * length
          }
        });

        gsap.to(".portrait1", {
          xPercent: 300,
          ease: 'none',
          scrollTrigger: {
            trigger: ".first-section",
            start: "center center",
            end: "right left",
            scrub: true,
            markers: true,

          }
        })

    }) //Her slutter next tick
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
    <section class="flex-none w-screen h-screen relative first-section">
      <img src="../../assets/Resting_web.jpg" class="portrait1 h-[90vh] translate-x-[10vw] translate-y-[5vh]">
    </section>
    <section class="flex-none w-screen h-screen bg-yellow-500/20 relative">
      
    </section>
    <section class="flex-none w-screen h-screen bg-purple-500 relative">
      
    </section>
  </div>
  </template>