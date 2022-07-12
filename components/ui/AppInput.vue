<template>
  <div>
    <input
      class="p-2 border-2 border-black rounded"
      :type="type"
      :placeholder="placeholder"
    />
  </div>
</template>
<script>
export default {
  name: 'AppInputText',
  props: {
    placeholder: {
      type: String,
      default: '',
    },
    type: {
      type: String,
      default: 'text',
    },
  },
  data() {
    return {}
  },
}
</script>
<style></style>
