<template>
  <div class="min-h-screen bg-gradient-to-b from-gray-900 to-gray-800 text-white pt-20">
    <!-- Hero Section -->
    <section class="py-24 relative overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <div class="absolute top-20 left-20 w-40 h-40 bg-primary-500/20 rounded-full blur-2xl animate-pulse-slow"></div>
        <div class="absolute bottom-20 right-20 w-32 h-32 bg-secondary-500/20 rounded-full blur-2xl animate-bounce-slow"></div>
      </div>
      
      <div class="container mx-auto px-6 text-center relative z-10">
        <h1 class="text-5xl md:text-7xl font-display font-bold mb-8 animate-fade-in">
          <span class="bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">
            About TechFlow
          </span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto leading-relaxed animate-slide-up">
          We are passionate innovators dedicated to transforming digital experiences through cutting-edge web technologies and creative design solutions.
        </p>
      </div>
    </section>

    <!-- Our Story -->
    <section class="py-24 bg-gradient-to-b from-gray-800 to-gray-900">
      <div class="container mx-auto px-6">
        <div class="grid md:grid-cols-2 gap-16 items-center">
          <div class="animate-slide-up">
            <h2 class="text-4xl font-display font-bold mb-6">
              <span class="bg-gradient-to-r from-primary-300 to-accent-300 bg-clip-text text-transparent">
                Our Story
              </span>
            </h2>
            <p class="text-gray-300 mb-6 leading-relaxed">
              Founded in 2020, TechFlow emerged from a simple vision: to bridge the gap between innovative technology and exceptional user experiences. Our journey began with a small team of passionate developers and designers who believed that every business deserves a digital presence that truly represents their vision.
            </p>
            <p class="text-gray-400 leading-relaxed">
              Today, we've grown into a full-service digital agency, but our core values remain unchanged: quality, innovation, and client satisfaction above all else.
            </p>
          </div>
          
          <div class="relative animate-fade-in">
            <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 to-secondary-500/20 rounded-2xl blur-xl"></div>
            <div class="relative glass-effect rounded-2xl p-8">
              <div class="bg-gradient-to-br from-primary-500 via-secondary-500 to-accent-500 rounded-xl h-80 flex items-center justify-center">
                <div class="text-center text-white">
                  <i class="fas fa-rocket text-6xl mb-4 opacity-80"></i>
                  <h3 class="text-2xl font-bold">Innovation First</h3>
                  <p class="text-white/80">Pushing boundaries daily</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <section class="py-24 bg-gradient-to-b from-gray-900 to-gray-800">
      <div class="container mx-auto px-6 text-center">
        <h2 class="text-4xl md:text-5xl font-display font-bold mb-16">
          <span class="bg-gradient-to-r from-secondary-300 to-accent-300 bg-clip-text text-transparent">
            Meet Our Team
          </span>
        </h2>
        
        <div class="grid md:grid-cols-3 gap-8">
          <div class="group glass-effect p-8 rounded-2xl transition-all duration-500 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-24 h-24 bg-gradient-to-r from-primary-500 to-primary-600 rounded-full mx-auto flex items-center justify-center text-2xl font-bold text-white">
                AH
              </div>
            </div>
            <h3 class="text-xl font-bold mb-2">Ahmed Hassan</h3>
            <p class="text-primary-300 mb-4">Lead Developer</p>
            <p class="text-gray-400 text-sm">Full-stack developer with 8+ years experience in modern web technologies.</p>
          </div>
          
          <div class="group glass-effect p-8 rounded-2xl transition-all duration-500 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-24 h-24 bg-gradient-to-r from-secondary-500 to-secondary-600 rounded-full mx-auto flex items-center justify-center text-2xl font-bold text-white">
                SM
              </div>
            </div>
            <h3 class="text-xl font-bold mb-2">Sara Mohamed</h3>
            <p class="text-secondary-300 mb-4">UI/UX Designer</p>
            <p class="text-gray-400 text-sm">Creative designer specializing in user-centered design and modern interfaces.</p>
          </div>
          
          <div class="group glass-effect p-8 rounded-2xl transition-all duration-500 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-24 h-24 bg-gradient-to-r from-accent-500 to-accent-600 rounded-full mx-auto flex items-center justify-center text-2xl font-bold text-white">
                MK
              </div>
            </div>
            <h3 class="text-xl font-bold mb-2">Mohamed Khalil</h3>
            <p class="text-accent-300 mb-4">Project Manager</p>
            <p class="text-gray-400 text-sm">Experienced PM ensuring projects are delivered on time and exceed expectations.</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
