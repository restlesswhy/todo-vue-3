<script setup lang="ts">
import { ref } from 'vue';

const title = ref('');
const description = ref('');

const onSubmit = () => {
    console.log(title.value)
    console.log(description.value)
}
</script>

<template>
    <div>
        <input v-model="title" type="name" placeholder="Title">
        <input v-model="description" type="description" placeholder="Description" style="margin-left: 5px;">
    </div>
    <button @click="onSubmit">create</button>
</template>