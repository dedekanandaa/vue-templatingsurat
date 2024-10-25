<script setup lang="ts">
import surat from "../api/surat.json"

interface Surat {
  nama: string;
  deskripsi: string;
}

const responses: Surat[] = surat.response

const isOpen = ref(false)
</script>

<template>
  <main class="max-w-screen-xl p-3 mx-auto sm:p-5 lg:px-12">
    <div class="flex justify-between w-full">
      <span class="content-end text-xl font-medium">
        Pilih Template Surat
      </span>
      <UButton color="gray" label="Open" @click="isOpen = true" class="flex items-center gap-2 p-2 text-sm text-gray-500 border-2 border-gray-300 rounded-md hover:bg-gray-100">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="size-4" fill="currentColor">
          <path d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 144L48 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l144 0 0 144c0 17.7 14.3 32 32 32s32-14.3 32-32l0-144 144 0c17.7 0 32-14.3 32-32s-14.3-32-32-32l-144 0 0-144z"/>
        </svg>
        New Template
      </UButton>
      
      <UModal v-model="isOpen">
        <div class="flex items-center justify-center w-full p-5">
            <label for="dropzone-file" class="flex flex-col items-center justify-center w-full h-64 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600">
                <div class="flex flex-col items-center justify-center pt-5 pb-6">
                    <svg class="w-8 h-8 mb-4 text-gray-500 dark:text-gray-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 16">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 13h3a3 3 0 0 0 0-6h-.025A5.56 5.56 0 0 0 16 6.5 5.5 5.5 0 0 0 5.207 5.021C5.137 5.017 5.071 5 5 5a4 4 0 0 0 0 8h2.167M10 15V6m0 0L8 8m2-2 2 2"/>
                    </svg>
                    <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                    <p class="text-xs text-gray-500 dark:text-gray-400">DOC or DOCX file</p>
                </div>
                <input id="dropzone-file" type="file" class="hidden" />
            </label>
        </div> 
      </UModal>
    </div>
    <section class="grid gap-5 pt-5 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
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

