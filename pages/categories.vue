<template>
  <main class="flex flex-col h-[80vh] mx-auto w-[90vw]">
    <section class="min-h-[30vh] space-y-3 justify-around pt-12">
      <h2 class="text-3xl">Categories</h2>
      <form class="flex space-x-3" @submit.prevent>
        <input
          class="p-2 border-2 border-black rounded"
          type="text"
          placeholder="Digite sua nova categoria"
        />
        <button class="bg-[#222] text-white p-3 rounded">Add</button>
      </form>
    </section>
    <section class="overflow-x-hidden min-h-[40vh]">
      <!-- LISTA -->
      <ul>
        <li class="flex justify-between pr-3 pb-4">
          <input
            v-if="edit"
            class="border-2 border-black rounded"
            type="text"
          />
          <span v-else>Categorie 1</span>
          <div class="space-x-2">
            <button class="text-sky-600">Edit</button>
            <button class="text-red-600">Delete</button>
          </div>
        </li>
      </ul>

      <!-- LISTA -->
    </section>
  </main>
</template>
<script>
export default {
  name: 'CategoriesPage',
  data() {
    return {
      edit: false,
    }
  },
}
</script>
<style></style>
