<template>
  <form>
    <!-- <input type="text" name="name" v-model="name" />
    <p v-if="nameError">{{ nameError }}</p> -->
    <InputField v-model="name" :error="nameError" name="name" />
    Vslue: {{ name }}
    <button type="submit" @click="onSubmit">Submit</button>
  </form>
</template>

<script>
import InputField from './InputField.vue'

import { useField, useForm } from 'vee-validate'
export default {
  name: 'ContactForm',

  setup() {
    const validations = {
      name: inputValue => !!inputValue
    }

    function onSubmit(e) {
      alert('submitted')
      e.preventDefault()
    }

    useForm({
      validationSchema: validations
    })

    // Need to do this for each field in the form
    const { value: name, errorMessage: nameError } = useField('name')

    return { onSubmit, nameError, name }
  },
  components: { InputField }
}
</script>
