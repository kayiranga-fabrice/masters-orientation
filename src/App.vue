<template>
  <div>
  <h1>Programming  learning orientation </h1>
    <form @submit.prevent="submitForm" class="custom-form">
      <div class="form-group">
        <label for="firstname">First Name:</label>
        <input type="text" id="firstname" v-model="formData.firstname" required>
      </div>
      
      <div class="form-group">
        <label for="secondname">Second Name:</label>
        <input type="text" id="secondname" v-model="formData.secondname" required>
      </div>
      
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="formData.email" required>
      </div>
      
      <div class="form-group">
        <label for="password">Password:</label>
        <input type="password" id="password" v-model="formData.password" required>
      </div>
      
      <div class="form-group">
        <button type="submit" class="submit-button">Submit</button>
        </div>
        <div>  <button type="button" @click="resetForm" class="reset-button">Reset password</button>  </div>
      
      
    </form>

    <img alt="Vue logo" src="https://vuejs.org/images/logo.png">
    <HelloWorld msg="EDISON trading floor"/>
    <HelloWorld msg="Welcome Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      formData: {
        firstname: '',
        secondname: '',
        email: '',
        password: '',
      }
    };
  },
  methods: {
    submitForm() {
      // Here you can perform actions like sending data to a server
      // or processing the form data in some way
      console.log('Form submitted with data:', this.formData);
      // Clear the form after submission
      this.formData.firstname = '';
      this.formData.secondname = '';
      this.formData.email = '';
      this.formData.password = '';
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* General styling for the form */
.custom-form {
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Style for each form group */
.form-group {
  margin-bottom: 15px;
}

/* Label style */
label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

/* Input field style */
input[type="text"],
input[type="email"],
input[type="password"] {
  width: 100%;
  padding: 6px; /* Adjusted padding */
  border: 1px solid #ccc;
  border-radius: 3px;
}

/* Style for submit and reset buttons */
.submit-button,
.reset-button {
  padding: 4px 15px;
  background-color: #2c3e50;
  color: white;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

/* Button hover effect */
.submit-button:hover,
.reset-button:hover {
  
  background-color: #34495e;
  
  .custom-heading {
  font-size: 28px; /* Adjust the font size */
  font-weight: bold;
  color: #2c3e50;
  margin-top: 20px; /* Add margin at the top */
}
}
</style>
