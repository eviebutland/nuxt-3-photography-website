<script>
export default defineComponent({
  data() {
    return {
      show: false
    }
  },
  mounted() {
    this.show // type: Boolean
  }
})
</script>

<template>
  <div>
    <h1>Mountains</h1>
    {{ show }}
    <LazyEventCard :event="{ time: 'now', id: 1, title: 'Evie events', date: '11/03/2022' }" />
    <button v-if="!show" @click="show = true">Show List</button>
  </div>
</template>
