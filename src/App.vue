<template>
<div>
    <router-view/>
</div>
</template>

<script>

import Home from '@/views/Home.vue'

export default {
    name: 'App',
    components: {
       Home
    },
    promps: {
      
    } 
}

</script>

<style >

body{
    background-color: #8fbfe0;

}
#myBtn {
    display: none; 
    position: fixed;
    bottom: 20px; 
    right: 30px; 
    z-index: 99; 
    border: none; 
    outline: none; 
    background-color: transparent; 
    color: rgb(255, 255, 255);
    cursor: pointer; 
    padding: 15px; 
    border-radius: 10px; 
    font-size: 18px; 
  }
  
  #myBtn:hover {
    background-color: rgba(203, 146, 146, 0.496); 
  }

@import '~bootstrap/dist/css/bootstrap.css';
</style>