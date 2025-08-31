<template>
  <div class="min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 text-white pt-20">
    <!-- Hero Section -->
    <section class="py-24 relative overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-20 left-20 w-40 h-40 bg-secondary-500/20 rounded-full blur-2xl animate-pulse-slow"></div>
        <div class="absolute bottom-20 right-20 w-32 h-32 bg-accent-500/20 rounded-full blur-2xl animate-bounce-slow"></div>
      </div>
      
      <div class="container mx-auto px-6 text-center relative z-10">
        <h1 class="text-5xl md:text-7xl font-display font-bold mb-8 animate-fade-in">
          <span class="bg-gradient-to-r from-secondary-300 to-accent-300 bg-clip-text text-transparent">
            Our Services
          </span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto leading-relaxed animate-slide-up">
          Comprehensive digital solutions tailored to elevate your business and create exceptional user experiences.
        </p>
      </div>
    </section>

    <!-- Services Grid -->
    <section class="py-24 bg-gradient-to-b from-gray-800 to-gray-900">
      <div class="container mx-auto px-6">
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Web Development -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-primary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-primary-500 to-primary-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-laptop-code text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-primary-300 transition-colors">Web Development</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Custom websites and web applications built with modern frameworks like React, Vue, and Next.js.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• Responsive Design</li>
              <li>• Performance Optimization</li>
              <li>• Cross-browser Compatibility</li>
              <li>• API Integration</li>
            </ul>
            <button class="w-full bg-primary-500/20 hover:bg-primary-500/30 border border-primary-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>

          <!-- UI/UX Design -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-accent-500 to-accent-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-accent-500 to-accent-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-paint-brush text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-accent-300 transition-colors">UI/UX Design</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Beautiful and intuitive designs that convert visitors into customers with exceptional user experiences.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• User Research</li>
              <li>• Wireframing & Prototyping</li>
              <li>• Visual Design</li>
              <li>• Usability Testing</li>
            </ul>
            <button class="w-full bg-accent-500/20 hover:bg-accent-500/30 border border-accent-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>

          <!-- SEO Optimization -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-secondary-500 to-secondary-600 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-secondary-500 to-secondary-600 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-chart-line text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-secondary-300 transition-colors">SEO Optimization</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Boost your search engine rankings and drive organic traffic with our proven SEO strategies.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• Keyword Research</li>
              <li>• On-page Optimization</li>
              <li>• Technical SEO</li>
              <li>• Performance Monitoring</li>
            </ul>
            <button class="w-full bg-secondary-500/20 hover:bg-secondary-500/30 border border-secondary-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>

          <!-- Mobile Development -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-accent-500 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-primary-500 to-accent-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-mobile-alt text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-primary-300 transition-colors">Mobile Development</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Native and cross-platform mobile applications for iOS and Android devices.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• iOS Development</li>
              <li>• Android Development</li>
              <li>• React Native</li>
              <li>• Flutter</li>
            </ul>
            <button class="w-full bg-primary-500/20 hover:bg-primary-500/30 border border-primary-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>

          <!-- E-commerce -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-secondary-500 to-accent-500 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-secondary-500 to-accent-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-shopping-cart text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-secondary-300 transition-colors">E-commerce Solutions</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Complete online store solutions with secure payment processing and inventory management.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• Custom Shopping Carts</li>
              <li>• Payment Integration</li>
              <li>• Inventory Management</li>
              <li>• Analytics & Reporting</li>
            </ul>
            <button class="w-full bg-secondary-500/20 hover:bg-secondary-500/30 border border-secondary-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>

          <!-- Consulting -->
          <div class="group glass-effect p-8 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-r from-accent-500 to-primary-500 rounded-full blur-lg opacity-20 group-hover:opacity-40 transition-opacity"></div>
              <div class="relative bg-gradient-to-r from-accent-500 to-primary-500 w-16 h-16 rounded-full flex items-center justify-center mx-auto">
                <i class="fas fa-lightbulb text-white text-2xl"></i>
              </div>
            </div>
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-accent-300 transition-colors">Digital Consulting</h3>
            <p class="text-gray-300 leading-relaxed mb-6">Strategic guidance to help you make informed decisions about your digital transformation journey.</p>
            <ul class="text-gray-400 text-sm space-y-2 mb-6">
              <li>• Technology Assessment</li>
              <li>• Digital Strategy</li>
              <li>• Architecture Planning</li>
              <li>• Performance Audits</li>
            </ul>
            <button class="w-full bg-accent-500/20 hover:bg-accent-500/30 border border-accent-500/30 px-6 py-3 rounded-lg transition-all duration-300">
              Learn More
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="py-24 bg-gradient-to-r from-primary-600 via-secondary-600 to-accent-600 text-center">
      <div class="container mx-auto px-6">
        <h2 class="text-4xl md:text-5xl font-display font-bold mb-6 text-white">
          Ready to Get Started?
        </h2>
        <p class="text-xl text-white/90 mb-8 max-w-2xl mx-auto">
          Let's discuss your project and find the perfect solution for your needs.
        </p>
        <button class="bg-white text-primary-600 px-10 py-4 rounded-full text-lg font-bold transition-all duration-300 transform hover:scale-105 shadow-2xl">
          Contact Us Today
        </button>
      </div>
    </section>
  </div>
</template>
