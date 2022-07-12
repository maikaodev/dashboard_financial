<template>
  <main class="mt-4 space-y-4 p-5 h-[80vh] overflow-x-hidden">
    <!-- HEADER -->
    <header>
      <div class="flex items-center justify-between">
        <h1 class="font-bold text-2xl">Categorias</h1>

        <AppButton @click="addCategory"> New </AppButton>
      </div>
    </header>
    <!-- HEADER -->
    <!-- FORM -->
    <form v-if="addNew" @submit.prevent>
      <ul class="md:flex items-center justify-between">
        <li>
          <AppFormLabel
            >Date
            <AppInputText v-model="form.date" type="date" />
          </AppFormLabel>
        </li>

        <li>
          <AppFormLabel
            >Value
            <AppInputText v-model="form.amount" type="number" />
          </AppFormLabel>
        </li>

        <li>
          <AppFormLabel
            >Description
            <AppInputText v-model="form.description" />
          </AppFormLabel>
        </li>

        <li>
          <AppFormLabel
            >Categories
            <AppFormSelect
              :options="[{ name: 'Licença de softwares', id: 1 }]"
            />
          </AppFormLabel>
        </li>
      </ul>

      <div class="space-x-4 flex items-center justify-end">
        <button
          class="inline-flex text-gray-700 text-sm"
          @click.stop.prevent="addCategory()"
        >
          Cancel
        </button>

        <AppButton @click="addTransaction"> Add </AppButton>
      </div>
    </form>
    <!-- FORM -->
    <!-- LIST -->
    <section class="mt-3">
      <header class="flex items-center space-x-4">
        <div class="flex items-center space-x-2">
          <fa class="text-lime-600" icon="plus" />

          <span class="font-bold">R$ 43,02</span>
        </div>

        <button>
          <fa icon="angle-down" />
        </button>
      </header>

      <div
        class="flex items-center px-5 py-6 bg-white space-x-5 rounded-lg shadow"
      >
        <span
          class="inline-flex items-center px-2.5 py-0.5 rounded-full text-sm font-medium bg-indigo-100 text-indigo-800"
        >
          Software
        </span>

        <p class="mt-1.5">Pagamento de boleto</p>
      </div>
    </section>
  </main>
</template>

<script>
import AppButton from '../components/ui/AppButton.vue'
import AppInputText from '../components/ui/AppInput.vue'
import AppFormLabel from '../components/ui/AppFormLabel.vue'
import AppFormSelect from '../components/ui/AppFormSelect.vue'

export default {
  name: 'TransactionsPage',
  components: { AppInputText, AppButton, AppFormLabel, AppFormSelect },

  data() {
    return {
      addNew: false,
      edit: false,
      form: {
        date: '',
        amount: 0,
        description: '',
        categoryId: '',
      },
      categories: [],
    }
  },
  methods: {
    addCategory() {
      this.addNew = !this.addNew
    },
    toggleEdit() {
      this.edit = !this.edit
    },
  },
}
</script>
<style></style>
