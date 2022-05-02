<template>
  compModel: {{ compModel.name }}
  <input type="text" :name="name" :value="compModel.name" />
  <p v-if="error">{{ error }}</p>
</template>

<script>
export default {
  name: 'InputField',
  props: {
    error: {
      type: String,
      default: ''
    },
    name: {
      type: String,
      default: ''
    }
  },
  setup() {
    const compModel = reactive({
      name: ''
    })

    return {
      compModel
    }
  }
}
</script>
