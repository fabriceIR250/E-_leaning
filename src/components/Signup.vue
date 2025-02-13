<template>
    <div class="container d-flex justify-content-center align-items-center vh-100">
      <div class="card p-4" style="width: 400px;">
        <h2 class="text-center">Sign Up</h2>
        <form @submit.prevent="register">
          <!-- Full Name Input with Icon -->
          <div class="mb-3">
            <label for="name" class="form-label">Full Name</label>
            <div class="input-group">
              <span class="input-group-text">
                <i class="fas fa-user"></i> <!-- Full Name Icon -->
              </span>
              <input type="text" id="name" class="form-control" v-model="name" required>
            </div>
          </div>
  
          <!-- Email Input with Icon -->
          <div class="mb-3">
            <label for="email" class="form-label">Email</label>
            <div class="input-group">
              <span class="input-group-text">
                <i class="fas fa-envelope"></i> <!-- Email Icon -->
              </span>
              <input type="email" id="email" class="form-control" v-model="email" required>
            </div>
          </div>
  
          <!-- Password Input with Icon -->
          <div class="mb-3">
            <label for="password" class="form-label">Password</label>
            <div class="input-group">
              <span class="input-group-text">
                <i class="fas fa-lock"></i> <!-- Password Icon -->
              </span>
              <input type="password" id="password" class="form-control" v-model="password" required>
            </div>
          </div>
  
          <!-- Sign Up Button with Icon -->
          <button type="submit" class="btn btn-primary w-100">
            <i class="fas fa-user-plus"></i> <!-- Sign Up Icon -->
            Sign Up
          </button>
        </form>
        <p class="text-center mt-3">Already have an account? <router-link to="/login">Login</router-link></p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        password: ''
      };
    },
    methods: {
      register() {
        console.log("Registering", this.name, this.email, this.password);
        // Here, you would handle registration logic (API request, etc.)
      }
    }
  };
  </script>
  
  <style>
  body {
    background-color: #f8f9fa;
  }
  .input-group-text {
    background-color: #e9ecef;
  }
  </style>
  