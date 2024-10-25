<script>
import surat from "../api/surat.json"

export default {
  data() {
    return {
      responses: surat.response,
    };
  }
};
</script>

<template>
  <main class="max-w-screen-xl p-3 mx-auto sm:p-5 lg:px-12">
    <div class="flex justify-between w-full">
      <span class="text-xl font-medium">
        Pilih Template Surat
      </span>
      <button class="flex items-center gap-2 p-2 text-gray-600 border-2 border-gray-600 rounded-md hover:bg-gray-100">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="size-4" fill="currentColor">
          <path d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 144L48 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l144 0 0 144c0 17.7 14.3 32 32 32s32-14.3 32-32l0-144 144 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l-144 0 0-144z"/>
        </svg>
        New Template
      </button>
    </div>
    <section class="grid grid-cols-4 gap-5 pt-5">
          <NuxtLink to="/surat" v-for="response in responses" class="p-4 bg-gray-100 border border-gray-200 rounded-md shadow-md hover:cursor-pointer hover:bg-gray-200">
              <div class="bg-center aspect-square">
                  <img src="../assets/surat.png" alt="" class="w-full h-full bg-cover rounded-sm">
              </div>
              <div class="items-center justify-center w-full py-3">
                  <h1 class="text-lg font-medium">{{ response.nama }}</h1>
                  <p class="text-gray-600">{{ response.deskripsi }}</p>
              </div>
          </NuxtLink>
      </section>
  </main>
</template>

