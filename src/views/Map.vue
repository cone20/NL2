<template>
  <div class="mapa">
    <Navbar />
    <br><br>
   <MAPS/>
    
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import MAPS from '@/components/MAPS.vue'



export default {
  name: 'Map',
  components: {
    Navbar,MAPS
  },
  props: {}
}
</script>

<style scoped>

body{
    background-color: rgb(161, 36, 36);
}

@import '~bootstrap/dist/css/bootstrap.css';
</style>
