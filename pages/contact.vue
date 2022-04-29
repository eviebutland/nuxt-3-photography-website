<script>
export default defineComponent({
  // type inference enabled
  props: {
    name: String,
    msg: { type: String, required: true }
  },
  data() {
    return {
      count: 1
    }
  },
  mounted() {
    this.name // type: string | undefined
    this.msg // type: string
    this.count // type: number
  }
})
</script>

<template>
  <p>Contact form here</p>
  <NuxtLink to="/">Home page</NuxtLink>
</template>
