<script>
export default {
  setup() {
    const counterRef = ref(0)
    return { counterRef }
  }
}
</script>

<template>
  <main>
    <h1>
      Evie here
      {{ counterRef }}
    </h1>
    <NuxtLink to="/contact">Get in contact</NuxtLink>
  </main>
</template>
