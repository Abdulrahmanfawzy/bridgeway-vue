<script setup lang="ts">
import MainFooter from './components/layout/MainFooter.vue';
import MainNavbar from './components/layout/MainNavbar.vue';
import HomePage from './pages/home/HomePage.vue';
</script>

<template>
  <MainNavbar />

  <main>
    <HomePage />
  </main>

  <MainFooter />
</template>

