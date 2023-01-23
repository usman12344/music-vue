<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar/Navbar.vue'
</script>

<template>
  <header>
    <Navbar />
  </header>

  <RouterView />
</template>


<style scoped>
.bg-red-100 {
  background-color: #F6673A;
}
</style>
