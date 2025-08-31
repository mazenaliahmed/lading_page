<template>
  <div class="min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 text-white pt-20">
    <!-- Hero Section -->
    <section class="py-24 relative overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-20 left-20 w-40 h-40 bg-accent-500/20 rounded-full blur-2xl animate-pulse-slow"></div>
        <div class="absolute bottom-20 right-20 w-32 h-32 bg-primary-500/20 rounded-full blur-2xl animate-bounce-slow"></div>
      </div>
      
      <div class="container mx-auto px-6 text-center relative z-10">
        <h1 class="text-5xl md:text-7xl font-display font-bold mb-8 animate-fade-in">
          <span class="bg-gradient-to-r from-accent-300 to-primary-300 bg-clip-text text-transparent">
            Get In Touch
          </span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto leading-relaxed animate-slide-up">
          Ready to start your project? Let's discuss how we can bring your vision to life.
        </p>
      </div>
    </section>

    <!-- Contact Form & Info -->
    <section class="py-24 bg-gradient-to-b from-gray-800 to-gray-900">
      <div class="container mx-auto px-6">
        <div class="grid md:grid-cols-2 gap-16">
          <!-- Contact Form -->
          <div class="animate-slide-up">
            <div class="glass-effect p-8 rounded-2xl shadow-2xl">
              <h2 class="text-3xl font-display font-bold mb-8">
                <span class="bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">
                  Send us a Message
                </span>
              </h2>
              
              <form class="space-y-6">
                <div class="grid md:grid-cols-2 gap-4">
                  <div>
                    <label class="block text-gray-300 mb-2">First Name</label>
                    <input type="text" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white placeholder-gray-400 focus:border-primary-400 transition-colors" placeholder="John">
                  </div>
                  <div>
                    <label class="block text-gray-300 mb-2">Last Name</label>
                    <input type="text" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white placeholder-gray-400 focus:border-primary-400 transition-colors" placeholder="Doe">
                  </div>
                </div>
                
                <div>
                  <label class="block text-gray-300 mb-2">Email</label>
                  <input type="email" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white placeholder-gray-400 focus:border-primary-400 transition-colors" placeholder="john@example.com">
                </div>
                
                <div>
                  <label class="block text-gray-300 mb-2">Phone</label>
                  <input type="tel" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white placeholder-gray-400 focus:border-primary-400 transition-colors" placeholder="+1 (555) 123-4567">
                </div>
                
                <div>
                  <label class="block text-gray-300 mb-2">Service</label>
                  <select class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white focus:border-primary-400 transition-colors">
                    <option value="">Select a service</option>
                    <option value="web-dev">Web Development</option>
                    <option value="ui-ux">UI/UX Design</option>
                    <option value="seo">SEO Optimization</option>
                    <option value="mobile">Mobile Development</option>
                    <option value="ecommerce">E-commerce</option>
                    <option value="consulting">Consulting</option>
                  </select>
                </div>
                
                <div>
                  <label class="block text-gray-300 mb-2">Message</label>
                  <textarea rows="5" class="w-full px-4 py-3 bg-white/10 border border-white/20 rounded-lg outline-none text-white placeholder-gray-400 focus:border-primary-400 transition-colors resize-none" placeholder="Tell us about your project..."></textarea>
                </div>
                
                <button type="submit" class="w-full bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-8 py-4 rounded-lg font-semibold transition-all duration-300 transform hover:scale-105 shadow-lg">
                  <span class="flex items-center justify-center">
                    Send Message
                    <i class="fas fa-paper-plane ml-2"></i>
                  </span>
                </button>
              </form>
            </div>
          </div>
          
          <!-- Contact Info -->
          <div class="animate-fade-in">
            <h2 class="text-3xl font-display font-bold mb-8">
              <span class="bg-gradient-to-r from-secondary-300 to-accent-300 bg-clip-text text-transparent">
                Contact Information
              </span>
            </h2>
            
            <div class="space-y-6 mb-12">
              <div class="flex items-center space-x-4 p-4 glass-effect rounded-xl">
                <div class="bg-gradient-to-r from-primary-500 to-primary-600 w-12 h-12 rounded-full flex items-center justify-center">
                  <i class="fas fa-envelope text-white"></i>
                </div>
                <div>
                  <h3 class="font-semibold text-white">Email</h3>
                  <p class="text-gray-300">hello@techflow.com</p>
                </div>
              </div>
              
              <div class="flex items-center space-x-4 p-4 glass-effect rounded-xl">
                <div class="bg-gradient-to-r from-secondary-500 to-secondary-600 w-12 h-12 rounded-full flex items-center justify-center">
                  <i class="fas fa-phone text-white"></i>
                </div>
                <div>
                  <h3 class="font-semibold text-white">Phone</h3>
                  <p class="text-gray-300">+1 (555) 123-4567</p>
                </div>
              </div>
              
              <div class="flex items-center space-x-4 p-4 glass-effect rounded-xl">
                <div class="bg-gradient-to-r from-accent-500 to-accent-600 w-12 h-12 rounded-full flex items-center justify-center">
                  <i class="fas fa-map-marker-alt text-white"></i>
                </div>
                <div>
                  <h3 class="font-semibold text-white">Address</h3>
                  <p class="text-gray-300">123 Tech Street, San Francisco, CA 94105</p>
                </div>
              </div>
              
              <div class="flex items-center space-x-4 p-4 glass-effect rounded-xl">
                <div class="bg-gradient-to-r from-primary-500 to-accent-500 w-12 h-12 rounded-full flex items-center justify-center">
                  <i class="fas fa-clock text-white"></i>
                </div>
                <div>
                  <h3 class="font-semibold text-white">Business Hours</h3>
                  <p class="text-gray-300">Mon - Fri: 9:00 AM - 6:00 PM</p>
                </div>
              </div>
            </div>
            
            <!-- Social Links -->
            <div>
              <h3 class="text-xl font-semibold mb-6 text-white">Follow Us</h3>
              <div class="flex space-x-4">
                <a href="#" class="w-12 h-12 bg-gradient-to-r from-blue-500 to-blue-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fab fa-facebook text-white"></i>
                </a>
                <a href="#" class="w-12 h-12 bg-gradient-to-r from-blue-400 to-blue-500 rounded-full flex items-center justify-center hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fab fa-twitter text-white"></i>
                </a>
                <a href="#" class="w-12 h-12 bg-gradient-to-r from-blue-600 to-blue-700 rounded-full flex items-center justify-center hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fab fa-linkedin text-white"></i>
                </a>
                <a href="#" class="w-12 h-12 bg-gradient-to-r from-gray-700 to-gray-800 rounded-full flex items-center justify-center hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fab fa-github text-white"></i>
                </a>
                <a href="#" class="w-12 h-12 bg-gradient-to-r from-pink-500 to-pink-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fab fa-instagram text-white"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Map Section -->
    <section class="py-24 bg-gradient-to-b from-gray-900 to-gray-800">
      <div class="container mx-auto px-6">
        <h2 class="text-4xl font-display font-bold text-center mb-12">
          <span class="bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">
            Find Us
          </span>
        </h2>
        
        <div class="glass-effect rounded-2xl p-8 shadow-2xl">
          <div class="bg-gradient-to-br from-primary-500/20 via-secondary-500/20 to-accent-500/20 rounded-xl h-96 flex items-center justify-center">
            <div class="text-center text-white">
              <i class="fas fa-map-marked-alt text-6xl mb-4 opacity-80"></i>
              <h3 class="text-2xl font-bold">Interactive Map</h3>
              <p class="text-white/80">San Francisco, California</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
// Contact form functionality can be added here
</script>
