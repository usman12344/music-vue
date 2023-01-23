<script setup>
import ItemCard from "@/components/ItemCard.vue";
import { ref } from "vue";

const items = ref([
    {id:1, title: 'Runtuh', penyanyi:'Febry Putri, Fiersa Bersari', image:'song-1.png'},
    {id:2, title: 'Takkan Hilang', penyanyi:'budi Doremi', image:'song-2.png'},
    {id:3, title: 'Apalah Arti Menunggu', penyanyi:'Raisa', image:'song-3.png'}
])

</script>


<template>
     <div class="container px-4 mx-auto my-16 md:px-12">
      <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Song</h2>
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <ItemCard v-for="item in items"
        :id="item.id"
        :key="item.key"
        :title="item.title"
        :penyanyi="item.penyanyi"
        :image="item.image"
        />
      </div>
    </div>
</template>