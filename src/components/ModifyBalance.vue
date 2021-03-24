<template>
  <button
    class="btn btn-primary"
    @click="action"
    :disabled="disable"
  >{{ text }}</button>
</template>

<script>
  export default {
    name: "ModifyBalance",
    props: {
      text: String,
      disable: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      action() {
        this.$emit('action');
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>