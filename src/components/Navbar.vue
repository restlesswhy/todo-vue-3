<script setup lang="ts">
import NavButton from './ui/navButton.vue'
</script>

<template>
    <div class="navbar">
        <div @click="$router.push('/')">Vue 3</div>
        <div class="navbar__btns">
            <NavButton @click="$router.push('/list')">List</NavButton>
        </div>
    </div>
</template>
  
  
<style scoped>
.navbar {
    height: 50px;
    background-color: lightgray;
    box-shadow: 2px 2px 4px gray;
    display: flex;
    align-items: center;
    padding: 0 15px;
}

.navbar__btns {
    margin-left: auto;
}
</style>