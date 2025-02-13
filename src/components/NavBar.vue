<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <router-link class="navbar-brand" to="/">
        <i class="fas fa-chalkboard-teacher"></i> E-Learning
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/">
              <i class="fas fa-home"></i> Home
            </router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/courses">
              <i class="fas fa-book"></i> Courses
            </router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/login">
              <i class="fas fa-sign-in-alt"></i> Login
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
};
</script>

<style scoped>
/* You can add custom styles for the navbar if needed */
.navbar .nav-link i {
  margin-right: 8px; /* Add space between the icon and text */
}
</style>
