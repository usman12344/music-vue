<script setup>
import { RouterLink } from 'vue-router';



</script>

<template>
    <div class="container p-2 mx-auto my-10 max-w-7xl">
      <div class="flex flex-row flex-wrap py-4">
        <main role="main" class="w-full px-4 pt-1 sm:w-2/3 md:w-2/3">
          <h1
            class="mb-2 text-3xl font-bold leading-normal tracking-tight text-gray-900 sm:text-4xl md:text-4xl"
          >
            Runtuh
          </h1>
          <p class="text-gray-500">feby Putri, Fiersa Bersari</p>
          <section id="gallery">
            <iframe width="420" height="345" src="https://www.youtube.com/embed/tgbNymZ7vqY" class="w-full mt-6 rounded-2xl">
            </iframe>
            <div class="grid grid-cols-4 gap-4 mt-4">
              <div class="overflow-hidden cursor-pointer rounded-2xl">
                <img src="@/assets/img/song-2.png" class="w-full" alt="">
              </div>
              <div class="overflow-hidden cursor-pointer ring-2 ring-indigo-500 rounded-2xl">
                <img src="@/assets/img/song-3.png" class="w-full" alt="">
              </div>
              <div class="overflow-hidden cursor-pointer rounded-2xl">
                <img src="@/assets/img/song-4.png" class="w-full" alt="">
              </div>
              <div class="overflow-hidden cursor-pointer rounded-2xl">
                <img src="@/assets/img/song-1.png" class="w-full" alt="">
              </div>
            </div>
          </section>
          <section class="" id="orders">
            <h1 class="mt-8 mb-3 text-lg font-semibold">About</h1>
            <div class="text-gray-500">
              <p class="pb-4">
                Sportly App UI Kit will help your Sport, Fitness, and Workout App
                products or services. Came with modern and sporty style, you can
                easily edit and customize all elements with components that can
                speed up your design process.
              </p>
              <p class="pb-4">
                Suitable for : <br>
                - Sport App <br>
                - Fitness & GYM App <br>
                - Workout App <br>
                - Trainer & Tracker App <br>
                - And many more <br>
              </p>
            </div>
          </section>
        </main>
        <aside class="w-full px-4 sm:w-1/3 md:w-1/3">
          <div class="sticky top-0 w-full pt-4 md:mt-24 ">
            <div class="p-6 border rounded-2xl">
              <div class="mb-4">
                <div class="flex mb-2">
                  <div>
                    <img src="@/assets/img/mp3.png" alt="" class="w-16" />
                  </div>
                  <div class="block mt-1 ml-4">
                    <h3 class="font-semibold text-md">MP3</h3>
                    <p class="text-gray-400 text-md">3:13</p>
                  </div>
                </div>
              </div>
              <RouterLink
                to="/success"
                class="inline-flex items-center justify-center w-full px-8 py-3 mb-4 text-base font-medium text-white bg-indigo-600 border border-transparent rounded-full hover:bg-indigo-700 md:py-2 md:text-md md:px-10 hover:shadow" 
              >
                Download Now
            </RouterLink>
              <div class="mb-4">
                <div class="flex mb-2">
                  <div>
                    <img src="@/assets/img/mp4.png" alt="" class="w-16" />
                  </div>
                  <div class="block mt-1 ml-4">
                    <h3 class="font-semibold text-md">MP4</h3>
                    <p class="text-gray-400 text-md">3:13</p>
                  </div>
                </div>
              </div>
              <RouterLink
                to="/success"
                class="inline-flex items-center justify-center w-full px-8 py-3 text-base font-medium text-white bg-indigo-600 border border-transparent rounded-full hover:bg-indigo-700 md:py-2 md:text-md md:px-10 hover:shadow"
              >
                Download Now
            </RouterLink>
            </div>
          </div>
        </aside>
      </div>
    </div>
</template>