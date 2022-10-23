<script setup>
import { ref } from 'vue';
import ItemsCard from '../ItemsCard.vue';

const items = ref([
    { id: 1, title: "Mobile UI Kit", category: "ajdsfj", image: "categories-2.jpg" },
    { id: 2, title: "Desktop UI Kit", category: "ajdsfj210", image: "categories-1.jpg" },
    { id: 3, title: "Apple UI Kit", category: "ajdsfj4123", image: "categories-3.jpg" },
    { id: 4, title: "People UI Kit", category: "ajdsfj348", image: "categories-4.jpg" },
])
</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <ItemsCard v-for="item in items" :key="item.id" :title="item.title" :category="item.category" :image="item.image" />
        </div>
    </div>
</template>