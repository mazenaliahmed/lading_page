<script setup lang="ts">
import HeroSection from '../components/home/HeroSection.vue'
import FeaturesSection from '../components/home/FeaturesSection.vue'
</script>

<template>
  <div class="bg-gray-900 text-white">
    <!-- Hero Section -->
    <HeroSection />
    <!-- Features Section -->
  
    <FeaturesSection />
    <!-- About Section -->
    <section class="py-20 bg-gray-900">
      <div class="container mx-auto px-6 grid md:grid-cols-2 gap-10 items-center">
        <img src="https://via.placeholder.com/500x300" alt="About" class="rounded-lg shadow-lg" />
        <div>
          <h2 class="text-3xl font-bold mb-4">About Our Company</h2>
          <p class="text-gray-300 mb-4">
            We are a team of passionate developers and designers dedicated to building high-quality websites.
          </p>
          <button class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-lg transition">Learn More</button>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section class="py-20 bg-gray-800">
      <div class="container mx-auto px-6 text-center">
        <h2 class="text-3xl font-bold mb-12">Our Services</h2>
        <div class="grid md:grid-cols-3 gap-8">
          <div class="p-6 bg-gray-700 rounded-lg shadow hover:shadow-lg transition">
            <i class="fas fa-laptop-code text-blue-400 text-4xl mb-4"></i>
            <h3 class="text-xl font-bold mb-2">Web Development</h3>
            <p class="text-gray-300">High-performance websites using modern frameworks.</p>
          </div>
          <div class="p-6 bg-gray-700 rounded-lg shadow hover:shadow-lg transition">
            <i class="fas fa-paint-brush text-pink-400 text-4xl mb-4"></i>
            <h3 class="text-xl font-bold mb-2">UI/UX Design</h3>
            <p class="text-gray-300">Beautiful and user-friendly designs for your brand.</p>
          </div>
          <div class="p-6 bg-gray-700 rounded-lg shadow hover:shadow-lg transition">
            <i class="fas fa-chart-line text-green-400 text-4xl mb-4"></i>
            <h3 class="text-xl font-bold mb-2">SEO Optimization</h3>
            <p class="text-gray-300">Rank higher and get more traffic to your site.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials -->
    <section class="py-20 bg-gray-900">
      <div class="container mx-auto px-6 text-center">
        <h2 class="text-3xl font-bold mb-12">What Our Clients Say</h2>
        <div class="grid md:grid-cols-3 gap-8">
          <div class="bg-gray-800 p-6 rounded-lg shadow">
            <p class="text-gray-300 mb-4">"Amazing service! Our website loads incredibly fast."</p>
            <h4 class="font-bold">Jane Doe</h4>
          </div>
          <div class="bg-gray-800 p-6 rounded-lg shadow">
            <p class="text-gray-300 mb-4">"Professional team and great support."</p>
            <h4 class="font-bold">John Smith</h4>
          </div>
          <div class="bg-gray-800 p-6 rounded-lg shadow">
            <p class="text-gray-300 mb-4">"Highly recommend for modern web projects."</p>
            <h4 class="font-bold">Sarah Lee</h4>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="py-20 bg-blue-600 text-center">
      <h2 class="text-3xl font-bold mb-4">Ready to start your project?</h2>
      <p class="mb-8">Let's build something amazing together.</p>
      <button class="bg-white text-blue-600 px-6 py-3 rounded-lg font-semibold hover:bg-gray-100 transition">
        Contact Us
      </button>
    </section>

    
  </div>
</template>
