<script setup lang="ts">
import { ref } from 'vue'
</script>

<template>
  <footer class="relative bg-gradient-to-r from-gray-900 via-gray-800 to-gray-900 text-white overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-br from-primary-500/20 to-secondary-500/20"></div>
    </div>
    
    <div class="relative z-10 container mx-auto px-6 py-16">
      <!-- Main Footer Content -->
      <div class="grid md:grid-cols-4 gap-8 mb-12">
        <!-- Brand Section -->
        <div class="md:col-span-1">
          <div class="flex items-center space-x-3 mb-6">
            <div class="bg-gradient-to-r from-primary-500 to-secondary-500 p-3 rounded-full">
              <i class="fas fa-rocket text-white text-xl"></i>
            </div>
            <span class="text-2xl font-display font-bold bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">TechFlow</span>
          </div>
          <p class="text-gray-300 mb-6 leading-relaxed">
            Building the future of web development with innovative solutions and cutting-edge technology.
          </p>
          <!-- Social Links -->
          <div class="flex space-x-4">
            <a href="#" class="w-10 h-10 bg-white/10 rounded-full flex items-center justify-center hover:bg-primary-500 transition-all duration-300 group">
              <i class="fab fa-facebook text-gray-300 group-hover:text-white"></i>
            </a>
            <a href="#" class="w-10 h-10 bg-white/10 rounded-full flex items-center justify-center hover:bg-primary-500 transition-all duration-300 group">
              <i class="fab fa-twitter text-gray-300 group-hover:text-white"></i>
            </a>
            <a href="#" class="w-10 h-10 bg-white/10 rounded-full flex items-center justify-center hover:bg-primary-500 transition-all duration-300 group">
              <i class="fab fa-linkedin text-gray-300 group-hover:text-white"></i>
            </a>
            <a href="#" class="w-10 h-10 bg-white/10 rounded-full flex items-center justify-center hover:bg-primary-500 transition-all duration-300 group">
              <i class="fab fa-github text-gray-300 group-hover:text-white"></i>
            </a>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-lg font-semibold mb-6 text-primary-300">Quick Links</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-gray-300 hover:text-primary-300 transition-colors">Home</a></li>
            <li><a href="#" class="text-gray-300 hover:text-primary-300 transition-colors">About Us</a></li>
            <li><a href="#" class="text-gray-300 hover:text-primary-300 transition-colors">Services</a></li>
            <li><a href="#" class="text-gray-300 hover:text-primary-300 transition-colors">Portfolio</a></li>
            <li><a href="#" class="text-gray-300 hover:text-primary-300 transition-colors">Contact</a></li>
          </ul>
        </div>

        <!-- Services -->
        <div>
          <h4 class="text-lg font-semibold mb-6 text-secondary-300">Services</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-gray-300 hover:text-secondary-300 transition-colors">Web Development</a></li>
            <li><a href="#" class="text-gray-300 hover:text-secondary-300 transition-colors">UI/UX Design</a></li>
            <li><a href="#" class="text-gray-300 hover:text-secondary-300 transition-colors">Mobile Apps</a></li>
            <li><a href="#" class="text-gray-300 hover:text-secondary-300 transition-colors">SEO Optimization</a></li>
            <li><a href="#" class="text-gray-300 hover:text-secondary-300 transition-colors">Consulting</a></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h4 class="text-lg font-semibold mb-6 text-accent-300">Get in Touch</h4>
          <div class="space-y-4">
            <div class="flex items-center space-x-3">
              <i class="fas fa-envelope text-accent-400"></i>
              <span class="text-gray-300">hello@techflow.com</span>
            </div>
            <div class="flex items-center space-x-3">
              <i class="fas fa-phone text-accent-400"></i>
              <span class="text-gray-300">+1 (555) 123-4567</span>
            </div>
            <div class="flex items-center space-x-3">
              <i class="fas fa-map-marker-alt text-accent-400"></i>
              <span class="text-gray-300">San Francisco, CA</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-white/10 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-gray-400 text-sm mb-4 md:mb-0">
            © 2025 TechFlow. All rights reserved.
          </p>
          <div class="flex space-x-6 text-sm">
            <a href="#" class="text-gray-400 hover:text-primary-300 transition-colors">Privacy Policy</a>
            <a href="#" class="text-gray-400 hover:text-primary-300 transition-colors">Terms of Service</a>
            <a href="#" class="text-gray-400 hover:text-primary-300 transition-colors">Cookie Policy</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
