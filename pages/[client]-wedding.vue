<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()

// definePageMeta({
//   title: `${route.params.client} Wedding`
// })

// console.log(route)
</script>

<template>
  <h1>{{ $route.params.client }} here</h1>
</template>
