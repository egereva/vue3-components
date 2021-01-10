<template>
  <button class="btn" :class="color" @click="$emit('action')">
    <slot/>
  </button>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: '',
      validator(value) {
        return ['', 'primary', 'danger'].includes(value)
      }
    }
  },
  emits: ['action'],
  methods: {
    btnLog() {
      console.log('Button log')
    }
  }
}
</script>

<style scoped>

</style>
