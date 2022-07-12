<template>
  <main class="flex flex-col mt-3 h-[80vh] mx-auto w-[90vw]">
    <header class="flex items-center justify-between">
      <h1 class="font-bold text-2xl">Categories</h1>
    </header>

    <section class="mt-6">
      <div>
        <div class="flex items-center space-x-3">
          <AppInputText placeholder="Write a new categorie" />
          <AppButton> Add </AppButton>
        </div>
      </div>

      <table class="mt-4 divide-y divide-gray-200 shadow">
        <thead class="bg-gray-50">
          <tr>
            <th
              scope="col"
              class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider"
            >
              Categorie
            </th>
            <th scope="col" class="relative px-6 py-3">
              <span class="sr-only">Edit</span>
            </th>
          </tr>
        </thead>
        <tbody class="bg-white divide-y divide-gray-200">
          <tr class="bg-white">
            <td
              class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900"
            >
              <AppFormInput />
            </td>

            <td
              class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium space-x-4"
            >
              <button class="text-indigo-600 hover:text-indigo-900">
                Edit
              </button>

              <a href="#" class="text-red-600 hover:text-red-900">Excluir </a>
            </td>
          </tr>

          <tr class="bg-white">
            <td
              class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900"
            >
              Categoria 2
            </td>

            <td
              class="px-6 py-4 whitespace-nowrap text-right text-sm font-medium space-x-4"
            >
              <button class="text-indigo-600 hover:text-indigo-900">
                Edit
              </button>

              <button class="text-red-600 hover:text-red-900">Excluir</button>
            </td>
          </tr>
        </tbody>
      </table>
    </section>
  </main>
</template>
<script>
import AppButton from '../components/ui/AppButton.vue'
import AppInputText from '../components/ui/AppInput.vue'
export default {
  name: 'CategoriesPage',
  components: { AppInputText, AppButton },
  data() {
    return {
      edit: false,
    }
  },
  methods: {
    toggleEdit() {
      this.edit = !this.edit
    },
  },
}
</script>
<style></style>
