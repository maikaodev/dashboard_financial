<template>
  <button class="bg-[#222] text-white p-3 rounded" @click="$emit('click')">
    <slot />
  </button>
</template>
<script>
export default {
  name: 'AppButton',

  data() {
    return {}
  },
}
</script>
<style></style>
