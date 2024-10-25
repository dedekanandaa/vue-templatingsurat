<script>
import test from "../../api/test.json"

export default {
  data() {
    return {
      title: test.title,
      placeholders: test.placeholder, 
    };
  }
};
</script>

<template>
    <section class="p-3 dark:bg-gray-900 sm:p-5">
    <div class="max-w-screen-xl px-4 mx-auto lg:px-12">
        <h1 class="pb-5 text-3xl">{{ title }}</h1>
        <div class="relative overflow-hidden bg-white shadow-md dark:bg-gray-800 sm:rounded-lg">
            <div class="overflow-x-auto">
                <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
                    <thead class="text-xs text-gray-700 uppercase bg-gray-100 dark:bg-gray-700 dark:text-gray-400">
                        <tr>
                            <th scope="col" class="px-4 py-3">Placeholder</th>
                            <th scope="col" class="px-4 py-3">Description</th>
                            <th scope="col" class="px-4 py-3">Typedata</th>
                            <th scope="col" class="px-4 py-3">Value</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="placeholder in placeholders" :key="placeholder.id" class="border-b dark:border-gray-700">
                            <td class="px-4 py-3">{{ placeholder.name }}</td>
                            <td class="px-4 py-3">{{ placeholder.description }}</td>
                            <td class="px-4 py-3">{{ placeholder.typedata }}</td>
                            <td class="px-4 py-3"> 
                                <input v-if="placeholder.typedata === 'text'" type="text" class="w-full p-1 border border-gray-300 rounded">
                                <input v-if="placeholder.typedata === 'date'" type="date" class="w-full p-1 border border-gray-300 rounded">
                                <input v-if="placeholder.typedata === 'number'" type="number" class="w-full p-1 border border-gray-300 rounded">
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
        <div class="flex justify-end w-full gap-3">
            <button class="px-6 py-2 my-3 text-white bg-blue-600 rounded hover:bg-blue-700">Preview</button>
            <button class="px-6 py-2 my-3 text-white bg-red-600 rounded hover:bg-red-700">Cancel</button>
            <button class="px-6 py-2 my-3 text-white bg-green-600 rounded hover:bg-green-700">Submit</button>
        </div>
    </div>
    </section>
</template>