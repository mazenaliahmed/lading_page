<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const handleGetStarted = () => {
  router.push('/contact')
}

const handleWatchDemo = () => {
  // Open demo video or modal
  window.open('https://www.youtube.com/watch?v=dQw4w9WgXcQ', '_blank')
}

const scrollToFeatures = () => {
  const element = document.getElementById('features')
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
    <!-- Animated Background -->
    <div class="absolute inset-0 gradient-bg"></div>
    
    <!-- Floating Elements -->
    <div class="absolute inset-0">
      <div class="absolute top-20 left-10 w-20 h-20 bg-primary-500/20 rounded-full blur-xl animate-bounce-slow"></div>
      <div class="absolute top-40 right-20 w-32 h-32 bg-secondary-500/20 rounded-full blur-xl animate-pulse-slow"></div>
      <div class="absolute bottom-20 left-1/4 w-16 h-16 bg-accent-500/20 rounded-full blur-xl animate-bounce-slow"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 container mx-auto px-6 text-center">
      <div class="animate-fade-in">
        <h1 class="text-5xl md:text-7xl lg:text-8xl font-display font-bold mb-8 leading-tight">
          <span class="bg-gradient-to-r from-white via-primary-200 to-secondary-200 bg-clip-text text-transparent">
            Build Your
          </span>
          <br>
          <span class="bg-gradient-to-r from-primary-300 via-secondary-300 to-accent-300 bg-clip-text text-transparent animate-gradient bg-300%">
            Dream Website
          </span>
        </h1>
        
        <p class="text-xl md:text-2xl text-white/80 mb-12 max-w-3xl mx-auto leading-relaxed animate-slide-up">
          We help you create modern, fast, and beautiful websites using the latest technologies. 
          Transform your ideas into stunning digital experiences.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center animate-slide-up">
          <button @click="handleGetStarted" class="group bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-8 py-4 rounded-full text-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-2xl hover:shadow-primary-500/25">
            <span class="flex items-center">
              Get Started Free
              <i class="fas fa-arrow-right ml-2 group-hover:translate-x-1 transition-transform"></i>
            </span>
          </button>
          
          <button @click="handleWatchDemo" class="group glass-effect px-8 py-4 rounded-full text-lg font-semibold transition-all duration-300 transform hover:scale-105 border border-white/30 hover:border-white/50">
            <span class="flex items-center text-white">
              <i class="fas fa-play mr-2 group-hover:scale-110 transition-transform"></i>
              Watch Demo
            </span>
          </button>
        </div>
        
        <!-- Stats -->
        <div class="grid grid-cols-3 gap-8 mt-16 max-w-2xl mx-auto">
          <div class="text-center animate-slide-up">
            <div class="text-3xl md:text-4xl font-bold text-white mb-2">500+</div>
            <div class="text-white/70">Projects</div>
          </div>
          <div class="text-center animate-slide-up">
            <div class="text-3xl md:text-4xl font-bold text-white mb-2">99%</div>
            <div class="text-white/70">Satisfaction</div>
          </div>
          <div class="text-center animate-slide-up">
            <div class="text-3xl md:text-4xl font-bold text-white mb-2">24/7</div>
            <div class="text-white/70">Support</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <button @click="scrollToFeatures" class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce hover:text-primary-300 transition-colors cursor-pointer">
      <i class="fas fa-chevron-down text-white/50 text-2xl hover:text-primary-300"></i>
    </button>
  </section>
</template>


