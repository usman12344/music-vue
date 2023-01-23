<script setup>
import ArtisCard from "@/components/ArtisCard.vue";
import { ref } from "vue";

const artis = ref([
    {
        id: 1,
        title: 'aaaaaaaaaa',
        count: 1,
        image: 'artis-1.png'
    },
    {
        id: 2,
        title: 'bbbbbb',
        count: 2,
        image: 'artis-2.png'
    },
    {
        id: 3,
        title: 'cccccccccc',
        count: 3,
        image: 'artis-3.png'
    },
    {
        id: 4,
        title: 'dddddd',
        count: 4,
        image: 'artis-4.png'
    },
])

</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
        <div class="text-center">
            <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-xl md:mb-6">All Artis</h2>
        </div>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <ArtisCard v-for="artiss in artis"
            :id="artiss.id"
            :key="artiss.id"
            :title="artiss.title"
            :count="artiss.count"
            :image="artiss.image"
            />
        </div>
    </div>
</template>