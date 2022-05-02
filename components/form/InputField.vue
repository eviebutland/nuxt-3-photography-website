<template>
  <div>
    compModel: {{ value }}
    <input type="text" :name="name" v-model="value" />
    <p v-if="error">{{ error }}</p>
  </div>
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
    },

    value: {
      type: String,
      default: ''
    }
  },
  setup(props) {
    console.log(props)
    // const compModel = computed({
    //   name: props.name
    // })
    // return {
    //   compModel
    // }
  }
}
</script>
