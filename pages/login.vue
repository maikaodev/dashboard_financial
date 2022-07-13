<template>
  <main
    class="flex flex-col items-center justify-center mt-12 h-[80vh] mx-auto w-[90vw]"
  >
    <section class="h-[60vh] md:w-1/3">
      <form @submit.prevent>
        <AppFormLabel>
          Email:
          <AppInput :type="email" placeholder="Email@example.com" />
        </AppFormLabel>
        <AppFormLabel>
          Password:
          <AppInput :type="password" placeholder="Password" />
        </AppFormLabel>
        <AppButton class="mt-4 w-full" @click="alert()">Login</AppButton>
      </form>
    </section>
  </main>
</template>
<script>
import AppFormLabel from '../components/ui/AppFormLabel.vue'
import AppInput from '../components/ui/AppInput.vue'
import AppButton from '../components/ui/AppButton.vue'
export default {
  name: 'LoginUser',
  components: {
    AppFormLabel,
    AppInput,
    AppButton,
  },
  data() {
    return {}
  },
  created() {
    console.log('Created')
  },
  methods: {
    alert() {
      alert('Logado')
    },
  },
}
</script>
<style></style>
