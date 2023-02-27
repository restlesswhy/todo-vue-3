<script setup lang="ts">
const props = defineProps<{
    title: string,
    description: string,
    isDone: boolean
}>()
</script>

<template>
    <div class="my_item">
        <p v-bind="props">TITLE: {{ props.title }}, DESCRIPTION: {{ props.description }}</p>
    </div>
</template>

<style>
.my_item {
    padding: 15px;
    border: 2px solid rgb(4, 97, 43);
    margin-top: 15px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>