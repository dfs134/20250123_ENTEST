<template>
  <header class="max-big-width">
    <Header/>
  </header>
  <main class="max-big-width">
    <RouterView/>
  </main>
  <footer class="bg-grey-10 q-py-lg">
    <Footer/>
  </footer>
</template>

<script setup>
import Header from './views/Header.vue'
import Footer from './views/Footer.vue'

</script>

<style lang="css" src="./assets/app.css"></style>
