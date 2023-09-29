<template>
  <div>
    <h1>Contact Me</h1>
    <p>
      Thank you very much for taking the time to view my portfolio. If you have any additional queries and questions or are looking to get in contact with me, please fill in this form, and I will endeavor to get in contact with you as soon as possible.
    </p>
    <form @submit.prevent="submitForm">
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="formData.name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" v-model="formData.email" required>

      <label for="message">Message:</label>
      <textarea id="message" v-model="formData.message" rows="4" required></textarea>

      <button type="submit">Submit</button>
    </form>

    <div v-if="submitted">
      <p>Thank you for your submission!</p>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      formData: {
        name: '',
        email: '',
        message: ''
      },
      submitted: false
    }
  },
  methods: {
    submitForm () {
      console.log('Form submitted with data:', this.formData)

      this.submitted = true
    }
  }
}
</script>
