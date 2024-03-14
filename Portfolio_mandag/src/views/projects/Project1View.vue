<script>
import { gsap } from "gsap";
    
    import { ScrollTrigger } from "gsap/ScrollTrigger";
    gsap.registerPlugin(ScrollTrigger);

/*let imgContainerElement = document.getElementById("image-container");*/

export default {
  mounted() {
    gsap.to("#image-container", {
      x: -300,

      scrollTrigger: {
        trigger: "body",
        markers: true,
        start: "top top",
        end: "1500px",
        scrub: 1,
        pin: true,
        
      
      }
    });
  }
}


</script>


<template>
  <body class="scroll h-screen">
   <div id="image-container" class="absolute">
    <img src="../../assets/Resting_web.jpg" class="grid h-[90vh] translate-x-[20vw] translate-y-[5vh]">
   </div>
  </body>
  </template>