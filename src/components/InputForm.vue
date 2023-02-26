<script setup lang="ts">
import { ref } from 'vue';

const name = ref('');
const description = ref('');

const onSubmit = () => {
    console.log(name.value)
    console.log(description.value)
}

</script>

<template>
    <input v-model="name" type="name">
    <input v-model="description" type="description">
    <button @click="onSubmit">create</button>
</template>