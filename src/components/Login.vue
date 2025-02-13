<template>
    <div class="container d-flex justify-content-center align-items-center vh-100">
      <div class="card p-4" style="width: 400px;">
        <h2 class="text-center">Login</h2>
        <form @submit.prevent="login">
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
  
          <!-- Login Button with Icon -->
          <button type="submit" class="btn btn-primary w-100" :disabled="loading">
            <i class="fas fa-sign-in-alt"></i> <!-- Login Icon -->
            {{ loading ? "Logging in..." : "Login" }}
          </button>
  
          <p v-if="errorMessage" class="text-danger text-center mt-2">{{ errorMessage }}</p>
        </form>
        <p class="text-center mt-3">Don't have an account? <router-link to="">Sign up</router-link></p>
      </div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        email: '',
        password: '',
        loading: false,
        errorMessage: ''
      };
    },
    methods: {
      async login() {
        this.loading = true;
        this.errorMessage = '';
  
        try {
          const response = await axios.get('https://jack-backend-production.up.railway.app/user', {
            email: this.email,
            password: this.password
          });
  
          console.log("Login successful:", response.data);
  
          // Handle successful login, e.g., store token and redirect
          localStorage.setItem('token', response.data.token);
          this.$router.push('/dashboard'); // Redirect after login
        } catch (error) {
          this.errorMessage = error.response?.data?.message || "Login failed. Please check your credentials.";
        } finally {
          this.loading = false;
        }
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
  