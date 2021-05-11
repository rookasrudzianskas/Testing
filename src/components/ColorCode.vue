<template>
  <div>
    <input type="text" v-model="colorCode" placeholder="Enter color code">
  </div>
</template>

<script>
export default {
  computed: {
    colorCode: {
      get() {
        return this.$store.state.colorCode
      },
      set(newValue) {
        this.$store.dispatch('setColorCode', newValue)
      }
    }
  },
}
</script>