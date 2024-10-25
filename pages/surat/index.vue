<script>
import maildetail from "../../api/detailsurat.json"

export default {
  data() {
    return {
      number : maildetail.number,
      title: maildetail.doc_title,
      description : maildetail.doc_desc,
      date : maildetail.doc_date,
      rev : maildetail.doc_rev,
    };
  }
};

const items = [{
  label: 'Getting Started',
  icon: 'i-heroicons-information-circle',
  defaultOpen: true,
  content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.'
},
{
    label: 'Installation',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.'
}]
</script>

<template>
    <section class="p-3 dark:bg-gray-900 sm:p-5">
    <div class="flex max-w-screen-xl px-4 mx-auto lg:px-12">
        <div>
            <h1 class="pb-5 text-3xl">{{ title }}</h1>
            <div>
                <img src="../../assets/surat.png" alt="">
            </div>
            <span class="grid gap-2">
                <UAccordion
    open-icon="i-heroicons-plus"
    close-icon="i-heroicons-minus"
    :items="[{ label: '1. What is Nuxt UI?', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '2. Getting Started', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '3. Theming', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '4. Components', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }]"
  />
            </span>
        </div>
        <div class="relative right-6">
            <button class="px-6 py-2 my-3 text-white bg-red-600 rounded hover:bg-red-700">Back</button>
            <button class="px-6 py-2 my-3 text-white bg-green-600 rounded ms-2 hover:bg-green-700">Select Template</button>
        </div>
    </div>
    </section>
</template>