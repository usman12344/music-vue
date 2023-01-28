<script setup>
import ArtisCard from "@/components/ArtisCard.vue";
import { ref,onMounted } from 'vue';
import axios from 'axios';

const artis = ref([])

async function getArtis() {
  try {
    const response = await axios.get('https://music.free.mockoapp.net/artis')
    artis.value = response.data.data
    // console.log(response.data)
  } catch (error) {
    console.log(error);
  }
}

onMounted(() => {
  getArtis()
  
})

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
            :count="artiss.artis_count"
            :image="artiss.thumbnails"
            />
        </div>
    </div>
</template>