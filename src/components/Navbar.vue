<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm">
    <div class="container">
      <!-- Logo -->
      <router-link class="navbar-brand fw-bold" to="/">
        <i class="fas fa-chalkboard-teacher"></i> E-Learning
      </router-link>

      <!-- Mobile Menu Toggle -->
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Navbar Links -->
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
          <li class="nav-item">
            <router-link class="btn btn-primary ms-2" to="/signup">
              <i class="fas fa-user-plus"></i> Sign Up
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
/* Navbar styles */
.navbar {
  padding: 12px 0;
}

/* Styling for icons inside links */
.navbar .nav-link i,
.navbar .btn i {
  margin-right: 6px;
}

/* Button for sign-up */
.navbar .btn {
  font-weight: bold;
}
</style>
