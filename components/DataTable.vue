<template>
  <div class="p-4 m-x-auto">
    <h2 class="text-2xl text-gray-400 mb-2">{{ title }}</h2>
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
      <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
        <thead
          class="
            text-xs text-gray-700
            uppercase
            bg-gray-50
            dark:bg-gray-700 dark:text-gray-400
          "
        >
          <tr>
            <th v-for="heading in headings" scope="col" class="px-6 py-3">
              {{ heading }}
            </th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="row in data"
            class="bg-white border-b dark:bg-gray-800 dark:border-gray-700"
          >
            <th
              scope="row"
              class="
                px-6
                py-4
                font-medium
                text-gray-900
                whitespace-nowrap
                dark:text-white
              "
            >
              {{ row.product_name }}
            </th>
            <td class="px-6 py-4">{{ row.color }}</td>
            <td class="px-6 py-4">{{ row.category }}</td>
            <td class="px-6 py-4">{{ row.price }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script setup lang="ts">
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  headings: {
    type: Object,
    required: true,
  },
  data: {
    type: Object,
    required: false,
  },
});
</script>
