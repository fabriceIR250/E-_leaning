<template>
    <div>
      <!-- Navbar -->
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
          <a class="navbar-brand" href="#">Dashboard</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard">
                  <i class="fas fa-home"></i> Home
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/courses">
                  <i class="fas fa-book"></i> Courses
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/profile">
                  <i class="fas fa-user"></i> Profile
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/live-classes">
                  <i class="fas fa-video"></i> Live Classes
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/quizzes">
                  <i class="fas fa-pen-alt"></i> Quizzes & Exercises
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/work">
                  <i class="fas fa-briefcase"></i> Work
                </router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/dashboard/logout">
                  <i class="fas fa-sign-out-alt"></i> Logout
                </router-link>
              </li>
            </ul>
          </div>
        </div>
      </nav>
  
      <!-- Main Content -->
      <div class="container p-4">
        <h2>Welcome to Your Dashboard</h2>
        <div class="row">
          <div class="col-md-4">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">Total Courses</h5>
                <p class="card-text">{{ stats.totalCourses }}</p>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">Completed Courses</h5>
                <p class="card-text">{{ stats.completedCourses }}</p>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card text-center">
              <div class="card-body">
                <h5 class="card-title">Pending Courses</h5>
                <p class="card-text">{{ stats.pendingCourses }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        stats: {
          totalCourses: 10,
          completedCourses: 4,
          pendingCourses: 6
        }
      };
    }
  };
  </script>
  
  <style>
  body {
    background-color: #f8f9fa;
  }
  </style>
  