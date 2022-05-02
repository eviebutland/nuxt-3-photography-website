<script>
import ContactForm from '~~/components/form/ContactForm.vue'

export default {
  name: 'ContactPage',
  setup() {
    const show = ref(false)

    return { show }
  },
  components: { ContactForm }
}
</script>

<template>
  <p>Contact form here</p>
  <NuxtLink to="/">Home page</NuxtLink>

  <ContactForm />
</template>
