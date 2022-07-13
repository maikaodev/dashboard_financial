<template>
  <main
    class="flex flex-col items-center justify-center mt-12 h-[80vh] mx-auto w-[90vw]"
  >
    <section class="h-[70vh] md:w-1/3">
      <h1 class="text-4xl mb-4">Signup:</h1>

      <form @submit.prevent>
        <AppFormLabel>
          Username:
          <AppInput :type="text" placeholder="@username" />
        </AppFormLabel>
        <AppFormLabel>
          Email:
          <AppInput :type="email" placeholder="Email@example.com" />
        </AppFormLabel>
        <AppFormLabel>
          Password:
          <AppInputPassword />
        </AppFormLabel>
        <AppFormLabel>
          Confirm password:
          <AppInputPassword />
        </AppFormLabel>
        <AppButton class="mt-4 w-full" @click="alert()">Confirm</AppButton>
      </form>
    </section>
  </main>
</template>
<script>
import AppButton from '../components/ui/AppButton.vue'
import AppInput from '../components/ui/AppInput.vue'
import AppInputPassword from '../components/ui/AppInputPassword.vue'
import AppFormLabel from '../components/ui/AppFormLabel.vue'
export default {
  name: 'SignupUser',
  components: {
    AppButton,
    AppInput,
    AppInputPassword,
    AppFormLabel,
  },
  data() {
    return {}
  },

  methods: {
    alert() {
      alert('Register')
    },
  },
}
</script>
<style></style>
