<template>
  <div>
    <div class="max-w-lg mx-auto bg-white p-6 rounded-md shadow-lg">
      <h1 class="text-3xl font-semibold mb-4">
        Student Attendance - {{ today }}
      </h1>

      <!-- Student List -->
      <div class="space-y-4">
        <div class="flex items-center justify-between">
          <label class="text-lg">Student 2</label>
          <div class="flex items-center space-x-2">
            <input
              type="checkbox"
              class="form-checkbox h-5 w-5 text-blue-500"
            />
            <input
              type="text"
              placeholder="Add comment"
              class="border rounded-md p-2"
            />
          </div>
        </div>
        <div class="flex items-center justify-between">
          <label class="text-lg">Student 3</label>
          <div class="flex items-center space-x-2">
            <input
              type="checkbox"
              class="form-checkbox h-5 w-5 text-blue-500"
            />
            <input
              type="text"
              placeholder="Add comment"
              class="border rounded-md p-2"
            />
          </div>
        </div>
        <div class="flex items-center justify-between">
          <label class="text-lg">Student 3</label>
          <div class="flex items-center space-x-2">
            <input
              type="checkbox"
              class="form-checkbox h-5 w-5 text-blue-500"
            />
            <input
              type="text"
              placeholder="Add comment"
              class="border rounded-md p-2"
            />
          </div>
        </div>
        <!-- Add more students as needed -->
      </div>

      <!-- Save Button -->
      <div class="mt-6">
        <button
          class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md"
        >
          Save Attendance
        </button>
      </div>
    </div>
  </div>
  <DataTable
    title="Students 1"
    :headings="['Product', 'Color', 'Category', 'Price']"
    :data="dataRows"
  />
  <div class="p-4 m-x-auto">
    <h2 class="text-2xl text-gray-400 mb-2">Products</h2>
    <div class="relative overflow-x-auto border">
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
            <th scope="col" class="px-6 py-3">Product name</th>
            <th scope="col" class="px-6 py-3">Color</th>
            <th scope="col" class="px-6 py-3">Category</th>
            <th scope="col" class="px-6 py-3">Price</th>
          </tr>
        </thead>
        <tbody>
          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
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
              Apple MacBook Pro 17"
            </th>
            <td class="px-6 py-4">Silver</td>
            <td class="px-6 py-4">Laptop</td>
            <td class="px-6 py-4">$2999</td>
          </tr>
          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
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
              Microsoft Surface Pro
            </th>
            <td class="px-6 py-4">White</td>
            <td class="px-6 py-4">Laptop PC</td>
            <td class="px-6 py-4">$1999</td>
          </tr>
          <tr class="bg-white dark:bg-gray-800">
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
              Magic Mouse 2
            </th>
            <td class="px-6 py-4">Black</td>
            <td class="px-6 py-4">Accessories</td>
            <td class="px-6 py-4">$99</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script setup lang="ts">
const dataRows = ref([
  {
    product_name: 'Laptop',
    color: 'Silver',
    category: 'Electronics',
    price: 999.99,
  },
  {
    product_name: 'Sneakers',
    color: 'Red',
    category: 'Footwear',
    price: 49.99,
  },
  {
    product_name: 'Bookshelf',
    color: 'Brown',
    category: 'Furniture',
    price: 199.99,
  },
  {
    product_name: 'Smartphone',
    color: 'Black',
    category: 'Electronics',
    price: 699.99,
  },
  {
    product_name: 'T-shirt',
    color: 'Blue',
    category: 'Apparel',
    price: 19.99,
  },
]);
</script>
