<script setup>
import ItemCard from "../ItemCard.vue";
import axios from "axios";
import { ref, onMounted } from "vue";
import { useRoute } from "vue-router";


const items = ref([])
const route = useRoute()

async function getItem(){
  try {
    const response = await axios.get('https://music.free.mockoapp.net/artis/'+ route.params.id)
    items.value = response.data.product
    console.log(response.data)
  } catch (error) {
    console.log(error)
  }
}

onMounted(() => {
  getItem()
})

</script>


<template>
     <div class="container px-4 mx-auto my-16 md:px-12">
      <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Song</h2> 
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <ItemCard v-for="item in items"
        :id="item.id"
        :key="item.id"
        :title="item.title"
        :penyanyi="item.penyanyi"
        :image="item.thumbnails"
        />
      </div>
    </div>
</template>