<script setup>
import home from './components/home.vue'
</script>

<template>
  <h1 class="team_name">YINLA</h1>
  <home></home>
</template>

<style scoped>
  .team_name{
    font-size: 60px;
    animation: openIn 1s ease-in-out; 
  }

  @keyframes openIn{
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
        

    }
</style>
