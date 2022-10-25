<script setup>
import { ref } from 'vue';
import CategoriesCard from '../CategoriesCard.vue';

const categories = ref([
    { id: 1, title: "Mobile UI Kit", count: 78, image: "categories-2.jpg" },
    { id: 2, title: "Desktop UI Kit", count: 39210, image: "categories-1.jpg" },
    { id: 3, title: "Apple UI Kit", count: 234123, image: "categories-3.jpg" },
    { id: 4, title: "People UI Kit", count: 72348, image: "categories-4.jpg" },
])
</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg" id="categories">Top Categories</h2>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <CategoriesCard v-for="category in categories" :key="category.id" :title="category.title"
                :count="category.count" :image="category.image" />
        </div>
    </div>
</template>