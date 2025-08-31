<script setup lang="ts">
import { useRouter } from 'vue-router'
import HeroSection from '../components/home/HeroSection.vue'
import FeaturesSection from '../components/home/FeaturesSection.vue'

const router = useRouter()

const navigateToAbout = () => {
  router.push('/about')
}

const navigateToServices = () => {
  router.push('/services')
}

const navigateToContact = () => {
  router.push('/contact')
}

const handleStartProject = () => {
  router.push('/contact')
}

const handleScheduleCall = () => {
  // Open calendar booking or contact form
  window.open('tel:+15551234567', '_self')
}

const handleServiceLearnMore = (service: string) => {
  router.push(`/services#${service}`)
}
</script>

<template>
  <div class="bg-gray-900 text-white">
    <!-- Hero Section -->
    <HeroSection />
    <!-- Features Section -->
  
    <FeaturesSection />
    <!-- About Section -->
    <section id="about" class="py-24 bg-gradient-to-b from-gray-800 to-gray-900 relative overflow-hidden">
      <!-- Background Elements -->
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-20 right-10 w-40 h-40 bg-primary-500/20 rounded-full blur-2xl"></div>
        <div class="absolute bottom-20 left-10 w-32 h-32 bg-secondary-500/20 rounded-full blur-2xl"></div>
      </div>
      
      <div class="container mx-auto px-6 grid md:grid-cols-2 gap-16 items-center relative z-10">
        <!-- Image Section -->
        <div class="relative animate-fade-in">
          <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 to-secondary-500/20 rounded-2xl blur-xl"></div>
          <div class="relative glass-effect rounded-2xl p-8 shadow-2xl">
            <div class="bg-gradient-to-br from-primary-500 via-secondary-500 to-accent-500 rounded-xl h-80 flex items-center justify-center">
              <div class="text-center text-white">
                <i class="fas fa-users text-6xl mb-4 opacity-80"></i>
                <h3 class="text-2xl font-bold">Our Team</h3>
                <p class="text-white/80">Passionate Developers</p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Content -->
        <div class="animate-slide-up">
          <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
            <span class="bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">
              About Our Company
            </span>
          </h2>
          <p class="text-xl text-gray-300 mb-6 leading-relaxed">
            We are a team of passionate developers and designers dedicated to building high-quality websites that drive results and exceed expectations.
          </p>
          <p class="text-gray-400 mb-8 leading-relaxed">
            With years of experience in cutting-edge technologies, we transform your vision into reality through innovative web solutions.
          </p>
          
          <!-- Stats -->
          <div class="grid grid-cols-2 gap-6 mb-8">
            <div class="text-center p-4 glass-effect rounded-xl">
              <div class="text-2xl font-bold text-primary-300">5+</div>
              <div class="text-gray-400 text-sm">Years Experience</div>
            </div>
            <div class="text-center p-4 glass-effect rounded-xl">
              <div class="text-2xl font-bold text-secondary-300">50+</div>
              <div class="text-gray-400 text-sm">Team Members</div>
            </div>
          </div>
          
          <button @click="navigateToAbout" class="group bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-8 py-4 rounded-full font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg">
            <span class="flex items-center">
              Learn More About Us
              <i class="fas fa-arrow-right ml-2 group-hover:translate-x-1 transition-transform"></i>
            </span>
          </button>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 bg-gradient-to-b from-gray-900 to-gray-800 relative overflow-hidden">
      <!-- Background Pattern -->
      <div class="absolute inset-0 opacity-5">
        <div class="absolute inset-0 bg-gradient-to-r from-primary-500/10 to-accent-500/10"></div>
      </div>
      
      <div class="container mx-auto px-6 text-center relative z-10">
        <div class="mb-16 animate-fade-in">
          <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
            <span class="bg-gradient-to-r from-primary-300 to-accent-300 bg-clip-text text-transparent">
              Our Services
            </span>
          </h2>
          <p class="text-xl text-gray-300 max-w-2xl mx-auto">
            Comprehensive solutions to bring your digital vision to life
          </p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
          <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-primary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-primary-500 to-primary-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-laptop-code text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-primary-300 transition-colors">Web Development</h3>
            <p class="text-gray-300 leading-relaxed mb-6">High-performance websites using modern frameworks like React, Vue, and Next.js for optimal user experience.</p>
            <button @click="handleServiceLearnMore('web-development')" class="text-primary-400 hover:text-primary-300 font-medium transition-colors">
              Learn More <i class="fas fa-arrow-right ml-1"></i>
            </button>
          </div>

          <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.1s;">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-accent-500 to-accent-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-accent-500 to-accent-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-paint-brush text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-accent-300 transition-colors">UI/UX Design</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Beautiful and user-friendly designs that convert visitors into customers with intuitive user experiences.</p>
            <button @click="handleServiceLearnMore('ui-ux-design')" class="text-accent-400 hover:text-accent-300 font-medium transition-colors">
              Learn More <i class="fas fa-arrow-right ml-1"></i>
            </button>
          </div>

          <div class="group p-8 glass-effect rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.2s;">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-secondary-500 to-secondary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-secondary-500 to-secondary-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-chart-line text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-secondary-300 transition-colors">SEO Optimization</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Rank higher on search engines and get more organic traffic with our proven SEO strategies.</p>
            <button @click="handleServiceLearnMore('seo-optimization')" class="text-secondary-400 hover:text-secondary-300 font-medium transition-colors">
              Learn More <i class="fas fa-arrow-right ml-1"></i>
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials -->
    <section class="py-24 bg-gradient-to-b from-gray-800 to-gray-900 relative overflow-hidden">
      <!-- Background Elements -->
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-10 left-20 w-32 h-32 bg-primary-500/20 rounded-full blur-2xl animate-pulse-slow"></div>
        <div class="absolute bottom-10 right-20 w-40 h-40 bg-accent-500/20 rounded-full blur-2xl animate-bounce-slow"></div>
      </div>
      
      <div class="container mx-auto px-6 text-center relative z-10">
        <div class="mb-16 animate-fade-in">
          <h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
            <span class="bg-gradient-to-r from-secondary-300 to-accent-300 bg-clip-text text-transparent">
              What Our Clients Say
            </span>
          </h2>
          <p class="text-xl text-gray-300 max-w-2xl mx-auto">
            Don't just take our word for it - hear from our satisfied clients
          </p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up">
            <div class="mb-6">
              <div class="flex justify-center mb-4">
                <div class="flex space-x-1">
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                </div>
              </div>
              <p class="text-gray-300 text-lg leading-relaxed mb-6 italic">
                "Amazing service! Our website loads incredibly fast and the design is absolutely stunning. Conversion rates increased by 40%."
              </p>
            </div>
            <div class="flex items-center justify-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-primary-500 to-primary-600 rounded-full flex items-center justify-center">
                <span class="text-white font-bold">JD</span>
              </div>
              <div class="text-left">
                <h4 class="font-bold text-white">Jane Doe</h4>
                <p class="text-gray-400 text-sm">CEO, TechStart</p>
              </div>
            </div>
          </div>

          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.1s;">
            <div class="mb-6">
              <div class="flex justify-center mb-4">
                <div class="flex space-x-1">
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                </div>
              </div>
              <p class="text-gray-300 text-lg leading-relaxed mb-6 italic">
                "Professional team and exceptional support. They delivered exactly what we needed, on time and within budget."
              </p>
            </div>
            <div class="flex items-center justify-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-secondary-500 to-secondary-600 rounded-full flex items-center justify-center">
                <span class="text-white font-bold">JS</span>
              </div>
              <div class="text-left">
                <h4 class="font-bold text-white">John Smith</h4>
                <p class="text-gray-400 text-sm">Founder, InnovateCorp</p>
              </div>
            </div>
          </div>

          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 animate-slide-up" style="animation-delay: 0.2s;">
            <div class="mb-6">
              <div class="flex justify-center mb-4">
                <div class="flex space-x-1">
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                  <i class="fas fa-star text-yellow-400"></i>
                </div>
              </div>
              <p class="text-gray-300 text-lg leading-relaxed mb-6 italic">
                "Highly recommend for modern web projects. The attention to detail and user experience is outstanding."
              </p>
            </div>
            <div class="flex items-center justify-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-accent-500 to-accent-600 rounded-full flex items-center justify-center">
                <span class="text-white font-bold">SL</span>
              </div>
              <div class="text-left">
                <h4 class="font-bold text-white">Sarah Lee</h4>
                <p class="text-gray-400 text-sm">Marketing Director, GrowthLab</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section id="contact" class="py-24 bg-gradient-to-r from-primary-600 via-secondary-600 to-accent-600 text-center relative overflow-hidden">
      <!-- Animated Background -->
      <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 via-secondary-500/20 to-accent-500/20 animate-gradient bg-300%"></div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-10 left-10 w-20 h-20 bg-white/10 rounded-full blur-xl animate-bounce-slow"></div>
        <div class="absolute bottom-10 right-10 w-32 h-32 bg-white/5 rounded-full blur-2xl animate-pulse-slow"></div>
        <div class="absolute top-1/2 left-1/4 w-16 h-16 bg-white/10 rounded-full blur-xl animate-bounce-slow"></div>
      </div>
      
      <div class="container mx-auto px-6 relative z-10">
        <div class="max-w-4xl mx-auto animate-fade-in">
          <h2 class="text-4xl md:text-6xl font-display font-bold mb-6 text-white leading-tight">
            Ready to Start Your
            <span class="block bg-gradient-to-r from-yellow-300 to-orange-300 bg-clip-text text-transparent">
              Dream Project?
            </span>
          </h2>
          <p class="text-xl md:text-2xl text-white/90 mb-12 max-w-2xl mx-auto leading-relaxed">
            Let's build something amazing together. Transform your vision into reality with our expert team.
          </p>
          
          <div class="flex flex-col sm:flex-row gap-6 justify-center items-center animate-slide-up">
            <button @click="handleStartProject" class="group bg-white text-primary-600 px-10 py-4 rounded-full text-lg font-bold transition-all duration-300 transform hover:scale-105 shadow-2xl hover:shadow-white/25">
              <span class="flex items-center">
                Start Your Project
                <i class="fas fa-rocket ml-2 group-hover:translate-x-1 transition-transform"></i>
              </span>
            </button>
            
            <button @click="handleScheduleCall" class="group glass-effect px-10 py-4 rounded-full text-lg font-semibold transition-all duration-300 transform hover:scale-105 border border-white/30 hover:border-white/50 text-white">
              <span class="flex items-center">
                <i class="fas fa-phone mr-2 group-hover:scale-110 transition-transform"></i>
                Schedule a Call
              </span>
            </button>
          </div>
          
          <!-- Trust Indicators -->
          <div class="mt-16 flex flex-wrap justify-center items-center gap-8 opacity-80">
            <div class="flex items-center space-x-2">
              <i class="fas fa-shield-alt text-green-300"></i>
              <span class="text-white/80">SSL Secured</span>
            </div>
            <div class="flex items-center space-x-2">
              <i class="fas fa-clock text-blue-300"></i>
              <span class="text-white/80">24/7 Support</span>
            </div>
            <div class="flex items-center space-x-2">
              <i class="fas fa-money-bill-wave text-yellow-300"></i>
              <span class="text-white/80">Money Back Guarantee</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    
  </div>
</template>
