<script setup lang="ts">
const inputEmitName = 'customInput'
const emits = defineEmits<{ 
    (e: typeof inputEmitName, value: string): void
}>();

const onInput = () => {
    emits(inputEmitName, target.value);
}
</script>

<template>
    <input class="input" @input="onInput">
</template>

<style scoped>
.input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
}
</style>