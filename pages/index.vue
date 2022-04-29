<script>
export default defineComponent({
  data() {
    return {
      count: 1
    }
  },
  mounted() {
    this.count // type: number
  }
})
</script>

<template>
  <h1>
    Evie here
    {{ count }}
  </h1>
</template>
