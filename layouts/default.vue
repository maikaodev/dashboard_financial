<template>
  <div>
    <header
      class="flex justify-around drop-shadow-2xl md:justify-between items-center h-[10vh]"
    >
      <!-- LOGO -->
      <div class="logo cursor-pointer ml-3">
        <NuxtLInk :to="{ name: IndexPage }">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
            />
          </svg>
        </NuxtLInk>
      </div>
      <!-- LOGO -->

      <!-- Menu de navegação -->

      <nav class="space-x-2 cursor-pointer md:mr-6 md:space-x-3">
        <NuxtLInk
          class="py-3 md:px-3 duration-300 hover:bg-gray-300"
          :to="{ name: IndexPage }"
          >Home</NuxtLInk
        >
        <NuxtLInk
          class="py-3 md:px-3 ease-in duration-300 hover:bg-gray-300"
          :to="{ name: IndexPage }"
          >Categories</NuxtLInk
        >
        <NuxtLInk
          class="py-3 md:px-3 duration-300 hover:bg-gray-300"
          :to="{ name: IndexPage }"
          >Transactions</NuxtLInk
        >
      </nav>

      <!-- Menu de navegação -->
    </header>

    <Nuxt class="bg-gray" />

    <footer class="flex flex-col justify-center items-center h-[10vh]">
      <nav class="text-2xl space-x-2">
        <a href="https://github.com/maikaodev" target="_blank">
          <fa :icon="['fab', 'github']" />
        </a>
        <a href="https://www.linkedin.com/in/maikaodev/" target="_blank">
          <fa :icon="['fab', 'linkedin']" />
        </a>
      </nav>
      <span>Developed by @maikaodev - © 2022</span>
    </footer>
  </div>
</template>
<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {}
  },
}
</script>
<style>
* {
  font-family: 'Roboto', sans-serif;
  box-sizing: border-box;
}
</style>
