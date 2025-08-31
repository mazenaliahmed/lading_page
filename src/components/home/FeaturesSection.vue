<script setup lang="ts">

</script>

<template>
  <section class="py-24 bg-gradient-to-b from-gray-900 to-gray-800 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-primary-500/20 to-secondary-500/20"></div>
    </div>
    
    <div class="container mx-auto px-6 relative z-10">
      <!-- Section Header -->
      <div class="text-center mb-16 animate-fade-in">
        <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
          <span class="bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">
            Why Choose Us?
          </span>
        </h2>
        <p class="text-xl text-gray-300 max-w-2xl mx-auto">
          We deliver exceptional results with cutting-edge technology and innovative solutions
        </p>
      </div>

      <!-- Features Grid -->
      <div class="grid md:grid-cols-3 gap-8">
        <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up">
          <div class="relative mb-6">
            <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-primary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
            <div class="relative bg-gradient-to-r from-primary-500 to-primary-600 w-16 h-16 rounded-full flex items-center justify-center">
              <i class="fas fa-bolt text-white text-2xl"></i>
            </div>
          </div>
          <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-primary-300 transition-colors">Fast Performance</h3>
          <p class="text-gray-300 leading-relaxed">Lightning-fast websites that load in milliseconds, ensuring optimal user experience and higher conversion rates.</p>
        </div>

        <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.1s;">
          <div class="relative mb-6">
            <div class="absolute inset-0 bg-gradient-to-r from-secondary-500 to-secondary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
            <div class="relative bg-gradient-to-r from-secondary-500 to-secondary-600 w-16 h-16 rounded-full flex items-center justify-center">
              <i class="fas fa-shield-alt text-white text-2xl"></i>
            </div>
          </div>
          <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-secondary-300 transition-colors">Secure & Reliable</h3>
          <p class="text-gray-300 leading-relaxed">Enterprise-grade security with 99.9% uptime guarantee. Your data and users are always protected.</p>
        </div>

        <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.2s;">
          <div class="relative mb-6">
            <div class="absolute inset-0 bg-gradient-to-r from-accent-500 to-accent-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
            <div class="relative bg-gradient-to-r from-accent-500 to-accent-600 w-16 h-16 rounded-full flex items-center justify-center">
              <i class="fas fa-code text-white text-2xl"></i>
            </div>
          </div>
          <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-accent-300 transition-colors">Clean Code</h3>
          <p class="text-gray-300 leading-relaxed">Well-structured, maintainable code following industry best practices for easy scaling and future updates.</p>
        </div>
      </div>
    </div>
  </section>
</template>


