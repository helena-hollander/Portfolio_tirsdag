<script>
export default {
    props: {
        image: String,
    },
}
</script>

<template>
    
<img v-bind:src="image" alt="" class="grayscale hover:grayscale-0">
    


</template>

