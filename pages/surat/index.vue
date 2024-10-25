<script setup lang="ts">
import maildetail from "../../api/detailsurat.json"

const data = {
  number: maildetail.doc_number,
  title: maildetail.doc_title,
  description: maildetail.doc_desc,
  date: maildetail.doc_date,
  rev: maildetail.doc_rev,
};

const items = [{ 
                label: 'Description', 
                content: maildetail.doc_desc,
                defaultOpen: true
            }, 
            { 
                label: 'Date', 
                content: maildetail.doc_date,
            }, 
            { 
                label: 'Version', 
                content: maildetail.doc_rev,
            }]

</script>

<template>
    <section class="p-3 dark:bg-gray-900 sm:p-5">
    <div class="max-w-screen-xl gap-5 px-4 mx-auto lg:px-12">
        <div>
            <div class="grid gap-5 lg:grid-cols-2">
                <img src="../../assets/surat.png" alt="">
                <div>
                    <h1 class="pb-5 text-3xl">{{ data.title }}</h1>
                    <span class="grid gap-2">
                        <UAccordion :items="items" :ui="{ wrapper: 'flex flex-col w-full' }">
                            <template #default="{ item, index, open }">
                            <UButton color="gray" variant="ghost" class="border-b border-gray-200 dark:border-gray-700" :ui="{ rounded: 'rounded-none', padding: { sm: 'p-3' } }">
                                <span class="truncate">{{ item.label }}</span>
                                <template #trailing>
                                <UIcon
                                    name="i-heroicons-chevron-right-16-solid"
                                    class="w-5 h-5 transition-transform duration-200 transform ms-auto"
                                    :class="[open && 'rotate-90']"
                                />
                                </template>
                            </UButton>
                            </template>
                        </UAccordion>
                        <div class="mt-4 justify-self-end">
                            <NuxtLink to="/" v class="px-6 py-2 my-3 text-white bg-red-600 rounded hover:bg-red-700">Back</NuxtLink>
                            <NuxtLink to="/surat/input" class="px-6 py-2 my-3 text-white bg-green-600 rounded ms-2 hover:bg-green-700">Select Template</NuxtLink>
                        </div>
                    </span>
                </div>
            </div>
        </div>
    </div>
    </section>
</template>