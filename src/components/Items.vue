<script setup lang="ts">
import { ref, onMounted } from 'vue';
import item from './Item.vue';
import axios from 'axios';

interface IItems {
    title: string,
    description: string,
    isDone: boolean
}

const items = ref<IItems[]>([])

onMounted(async () => {
    const response = await axios
        .get(
            "http://localhost:8081/api/items/"
        )
        .then((res) => res.data)
        .catch((err) => console.error(err));

    console.log(response)
        // const itemList = response.map((item: any) => ({
        //     title: item.Title,
        //     description: item.Description,
        //     isDone: item.isDone,
        // }));

        // console.log(itemList)
    // items.value = [
    //     {
    //         title: "asdasd",
    //         description: "dddd",
    //         isDone: false
    //     },
    //     {
    //         title: "asdsdasd",
    //         description: "dddd",
    //         isDone: false
    //     }
    // ]
});

</script>

<template>
    <li v-for="item in items">
        <item :title="item.title" :description="item.description" :is-done=item.isDone></item>
    </li>
</template>