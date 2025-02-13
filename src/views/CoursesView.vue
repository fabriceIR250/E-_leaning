
<template>
  <Navbar />
    <div class="container my-5">
      <h2 class="text-center">All Courses</h2>
      <div class="row">
        <div class="col-md-4" v-for="course in courses" :key="course.id">
          <div class="card">
            <img :src="course.image" class="card-img-top" alt="Course Image">
            <div class="card-body">
              <h5 class="card-title">{{ course.title }}</h5>
              <p class="card-text">{{ course.description }}</p>
              <router-link :to="`/courses/${course.id}`" class="btn btn-primary">View Course</router-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--- Footer -->
    <Footer />
  </template>
  
  <script>
  import Footer from "@/components/Footer.vue";
import Navbar from "../components/Navbar.vue";
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
  