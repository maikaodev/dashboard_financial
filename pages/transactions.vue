<template>
  <main
    class="overflow-x-hidden flex flex-col h-[80vh] mx-2 md:mx-auto md:w-[90vw]"
  >
    <section class="space-y-3 justify-around pt-12">
      <!-- HEADER -->
      <div class="flex justify-between">
        <h2 class="text-3xl">Transactions</h2>
        <button
          class="bg-[#222] text-white p-3 rounded"
          @click="toggleNewTransaction()"
        >
          New
        </button>
      </div>
      <!-- HEADER -->
      <!-- FORM -->
      <form
        v-if="addNew"
        class="flex flex-col space-y-3 border-2 border-black rounded p-3 md:flex-row md:justify-between md:items-center md:space-y-0"
        @submit.prevent
      >
        <label
          >Date:
          <input type="date" />
        </label>
        <label
          >Value:
          <input class="border-2 border-black rounded" type="number" />
        </label>
        <label>
          Description:
          <input class="border-2 border-black rounded" type="text" />
        </label>
        <label>
          Categorie:
          <select name="" id="">
            <option value="">opt1</option>
            <option value="">opt1</option>
            <option value="">opt1</option>
            <option value="">opt1</option>
          </select>
        </label>

        <div class="flex self-end space-x-2">
          <button
            class="bg-red-600 p-2 rounded font-semibold"
            @click="toggleNewTransaction()"
          >
            Cancel
          </button>
          <button class="bg-green-600 p-2 rounded font-semibold">
            Confirmar
          </button>
        </div>
      </form>
      <!-- FORM -->
    </section>
    <section class="space-y-3 justify-around pt-12">
      <ul>
        <li
          class="flex flex-col py-3 border-t-2 border-indigo-500 mb-3 shadow-lg shadow-indigo-500/50"
        >
          <span class="self-end">$40,05</span>
          <div class="space-y-3">
            <span class="bg-indigo-400 p-1 rounded font-semibold"
              >Software</span
            >
            <p>Pagamento de boleto</p>
          </div>
          <div class="flex items-center self-end cursor-pointer space-x-3">
            <button class="text-sky-600 p-4">
              <fa icon="pen" />
            </button>
            <button class="text-red-600 p-4">
              <fa icon="x" />
            </button>
          </div>
        </li>
      </ul>
    </section>
  </main>
</template>
<script>
export default {
  name: 'TransactionsPage',
  data() {
    return {
      addNew: false,
    }
  },
  methods: {
    toggleNewTransaction() {
      this.addNew = !this.addNew
    },
  },
}
</script>
<style></style>
