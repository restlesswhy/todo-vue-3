<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
</script>

<template>
  <navbar></navbar>
  <div class="app">
    <router-view></router-view>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>