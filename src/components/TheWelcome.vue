<template>
  <div>
    <!-- Navbar -->
    <Navbar />

    <!-- Hero Section -->
    <header class="bg-primary text-white text-center py-5">
      <div class="container">
        <h1>Welcome to E-Learning</h1>
        <p>Learn from the best instructors online.</p>
        <a href="#" class="btn btn-light">Browse Courses</a>
      </div>
    </header>

    <!-- Course List -->
    <section class="container my-5">
      <h2 class="text-center">Popular Courses</h2>
      <div class="row">
        <div class="col-md-4" v-for="course in courses" :key="course.id">
          <div class="card">
            <img :src="course.image" class="card-img-top" alt="Course Image">
            <div class="card-body">
              <h5 class="card-title">
                <i class="fas fa-laptop-code"></i> <!-- Icon before course title -->
                {{ course.title }}
              </h5>
              <p class="card-text">{{ course.description }}</p>
              <a href="#" class="btn btn-primary">
                <i class="fas fa-arrow-right"></i> View Course <!-- Icon for the button -->
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";

export default {
  components: {
    Navbar,
    Footer
  },
  data() {
    return {
      courses: [
        { id: 1, title: "Vue.js Basics", description: "Learn the basics of Vue.js", image: "https://via.placeholder.com/300" },
        { id: 2, title: "Node.js for Beginners", description: "Start building backend applications", image: "https://via.placeholder.com/300" },
        { id: 3, title: "MySQL Database Management", description: "Master database design", image: "https://via.placeholder.com/300" }
      ]
    };
  }
};
</script>

<style scoped>
/* Add custom styles if needed */
header {
  background-image: url('https://via.placeholder.com/1200x400'); /* Example background image */
  background-size: cover;
  background-position: center;
}

.card-img-top {
  height: 200px;
  object-fit: cover;
}

footer {
  background-color: #f8f9fa;
  padding: 20px 0;
  text-align: center;
}
</style>
