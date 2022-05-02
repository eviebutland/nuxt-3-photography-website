<template>
  <form>
    <InputField v-model="name" :error="nameError" name="name" />
    <InputField v-model="email" :error="emailError" name="email" />

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
      name: inputValue => {
        console.log(inputValue)
        return !!inputValue ?? 'Please enter a name'
      },
      email: inputValue => !!inputValue
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
    const { value: email, errorMessage: emailError } = useField('email')

    return { onSubmit, nameError, name, email, emailError }
  },
  components: { InputField }
}
</script>
