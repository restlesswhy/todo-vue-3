<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
</script>

<template>
  <navbar></navbar>
  <div class="app">
    <router-view></router-view>
  </div>
</template>