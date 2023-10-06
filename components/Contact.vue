<template>
  <div class="contact">
    <h2>Contact</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="formData.name" required>
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="formData.email" required>
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" v-model="formData.message" required></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: '',
      },
    };
  },
  methods: {
    submitForm() {
      // You can handle form submission logic here,
      // such as sending the form data to a server.
      console.log('Form submitted with data:', this.formData);
      // You can add more logic to send the data to a server or perform other actions.
    },
  },
};
</script>

<style scoped>
/* Add CSS styles for the contact component here */
.contact {
  /* Add styles for the contact container */
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input
