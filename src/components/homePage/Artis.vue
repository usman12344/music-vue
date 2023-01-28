<script setup>
import ArtisCard from '@/components/ArtisCard.vue'
import { ref,onMounted } from 'vue';
import axios from 'axios';

const artis = ref([])

async function getArtis() {
  try {
    const response = await axios.get('https://music.free.mockoapp.net/artis/page=1&limit=4')
    artis.value = response.data.data
    console.log(response)
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
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-xl md:mb-6">Choose Your Artis</h2>
        <div class="flex justify-center mx-auto mb-4">
          <button class="px-6 py-2 text-white bg-black rounded-full hover:bg-blue-600">Pop</button>
          <button class="px-6 py-2 text-gray-400 border rounded-full hover:bg-blue-600">Jazz</button>
          <button class="px-6 py-2 text-gray-400 border rounded-full hover:bg-blue-600">Rock</button>
          <button class="px-6 py-2 text-gray-400 border rounded-full hover:bg-blue-600">Hip - Hop</button>
        </div>
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