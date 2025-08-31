<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const isMobileMenuOpen = ref(false)
const isSearchOpen = ref(false)
const searchQuery = ref('')
const isProfileMenuOpen = ref(false)

// Close menus when clicking outside
const handleClickOutside = (event: Event) => {
  const target = event.target as HTMLElement
  if (!target.closest('.mobile-menu') && !target.closest('.mobile-menu-button')) {
    isMobileMenuOpen.value = false
  }
  if (!target.closest('.profile-menu') && !target.closest('.profile-button')) {
    isProfileMenuOpen.value = false
  }
}

onMounted(() => {
  document.addEventListener('click', handleClickOutside)
})

onUnmounted(() => {
  document.removeEventListener('click', handleClickOutside)
})

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const toggleSearch = () => {
  isSearchOpen.value = !isSearchOpen.value
  if (isSearchOpen.value) {
    // Focus on search input after opening
    setTimeout(() => {
      const searchInput = document.querySelector('#search-input') as HTMLInputElement
      if (searchInput) searchInput.focus()
    }, 100)
  }
}

const toggleProfileMenu = () => {
  isProfileMenuOpen.value = !isProfileMenuOpen.value
}

const navigateTo = (route: string) => {
  router.push(route)
  isMobileMenuOpen.value = false
  isProfileMenuOpen.value = false
}

const scrollToSection = (sectionId: string) => {
  // If we're not on home page, navigate to home first
  if (router.currentRoute.value.path !== '/') {
    router.push('/').then(() => {
      setTimeout(() => {
        const element = document.getElementById(sectionId)
        if (element) {
          element.scrollIntoView({ behavior: 'smooth' })
        }
      }, 100)
    })
  } else {
    const element = document.getElementById(sectionId)
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' })
    }
  }
  isMobileMenuOpen.value = false
  isProfileMenuOpen.value = false
}

const handleNavigation = (type: 'route' | 'section', target: string) => {
  if (type === 'route') {
    navigateTo(target)
  } else {
    scrollToSection(target)
  }
}

const handleSearch = () => {
  if (searchQuery.value.trim()) {
    // Enhanced search functionality
    const query = searchQuery.value.toLowerCase()
    
    // Search logic based on keywords
    if (query.includes('web') || query.includes('development')) {
      navigateTo('/services')
      showNotification('Redirecting to Web Development services', 'success')
    } else if (query.includes('design') || query.includes('ui') || query.includes('ux')) {
      navigateTo('/services')
      showNotification('Redirecting to UI/UX Design services', 'success')
    } else if (query.includes('about') || query.includes('team') || query.includes('company')) {
      navigateTo('/about')
      showNotification('Redirecting to About page', 'success')
    } else if (query.includes('contact') || query.includes('phone') || query.includes('email')) {
      navigateTo('/contact')
      showNotification('Redirecting to Contact page', 'success')
    } else {
      // Default search behavior
      showNotification(`Searching for: ${searchQuery.value}`, 'info')
    }
    
    toggleSearch()
    searchQuery.value = ''
  }
}

const handleGetStarted = () => {
  navigateTo('/contact')
}

const handleLogout = () => {
  // Implement logout functionality
  console.log('Logging out...')
  isProfileMenuOpen.value = false
  // Clear user session/token here
  alert('Logged out successfully!')
}

// Add notification system
const showNotification = (message: string, type: 'success' | 'error' | 'info' = 'info') => {
  // Simple notification - can be enhanced with a proper toast system
  console.log(`${type.toUpperCase()}: ${message}`)
}
</script>

<template>
  <header class="sticky top-0 z-50 glass-effect backdrop-blur-md bg-white/10 text-white shadow-2xl border-b border-white/20">
    <div class="container mx-auto px-4">
      <div class="flex items-center justify-between h-20">
        <!-- Logo -->
        <button @click="navigateTo('/')" class="flex items-center space-x-3 animate-fade-in hover:scale-105 transition-transform duration-300">
          <div class="relative">
            <div class="absolute inset-0 bg-gradient-to-r from-primary-500 to-secondary-500 rounded-full blur-sm opacity-75"></div>
            <div class="relative bg-gradient-to-r from-primary-500 to-secondary-500 p-3 rounded-full">
              <i class="fas fa-rocket text-white text-xl"></i>
            </div>
          </div>
          <span class="text-2xl font-display font-bold bg-gradient-to-r from-primary-300 to-secondary-300 bg-clip-text text-transparent">TechFlow</span>
        </button>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center space-x-2">
          <button @click="navigateTo('/')" class="px-5 py-2.5 flex items-center rounded-full hover:bg-white/10 transition-all duration-300 group">
            <i class="fas fa-home mr-2 text-primary-300 group-hover:text-primary-200 transition-colors"></i> 
            <span class="font-medium">Home</span>
          </button>
          <button @click="navigateTo('/about')" class="px-5 py-2.5 flex items-center rounded-full hover:bg-white/10 transition-all duration-300 group">
            <i class="fas fa-info-circle mr-2 text-primary-300 group-hover:text-primary-200 transition-colors"></i> 
            <span class="font-medium">About</span>
          </button>
          <button @click="navigateTo('/services')" class="px-5 py-2.5 flex items-center rounded-full hover:bg-white/10 transition-all duration-300 group">
            <i class="fas fa-cogs mr-2 text-primary-300 group-hover:text-primary-200 transition-colors"></i> 
            <span class="font-medium">Services</span>
          </button>
          <button @click="navigateTo('/contact')" class="px-5 py-2.5 flex items-center rounded-full hover:bg-white/10 transition-all duration-300 group">
            <i class="fas fa-envelope mr-2 text-primary-300 group-hover:text-primary-200 transition-colors"></i> 
            <span class="font-medium">Contact</span>
          </button>
        </nav>

        <!-- Right Section -->
        <div class="flex items-center space-x-4">
          <!-- Search Icon -->
          <button @click="toggleSearch" class="p-3 rounded-full hover:bg-white/10 transition-all duration-300 group">
            <i class="fas fa-search text-primary-300 group-hover:text-primary-200 transition-colors"></i>
          </button>

          <!-- CTA Button -->
          <button @click="handleGetStarted" class="hidden md:block bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-6 py-2.5 rounded-full font-medium transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
            Get Started
          </button>

          <!-- Profile -->
          <div class="hidden lg:flex items-center space-x-3 relative profile-menu">
            <button @click="toggleProfileMenu" class="profile-button flex items-center space-x-3 cursor-pointer hover:bg-white/10 p-3 rounded-full transition-all duration-300">
              <div class="bg-gradient-to-r from-accent-500 to-accent-600 rounded-full w-10 h-10 flex items-center justify-center shadow-lg">
                <i class="fas fa-user text-white"></i>
              </div>
              <span class="font-medium">John Doe</span>
              <i class="fas fa-chevron-down text-sm transition-transform" :class="isProfileMenuOpen ? 'rotate-180' : ''"></i>
            </button>
            
            <!-- Profile Dropdown -->
            <div v-show="isProfileMenuOpen" class="absolute top-full right-0 mt-2 w-48 glass-effect rounded-xl shadow-2xl border border-white/20 py-2 animate-fade-in">
              <button @click="navigateTo('/profile')" class="w-full text-left px-4 py-3 hover:bg-white/10 transition-colors flex items-center">
                <i class="fas fa-user-circle mr-3 text-primary-300"></i>
                Profile
              </button>
              <button @click="navigateTo('/settings')" class="w-full text-left px-4 py-3 hover:bg-white/10 transition-colors flex items-center">
                <i class="fas fa-cog mr-3 text-secondary-300"></i>
                Settings
              </button>
              <button @click="navigateTo('/favorites')" class="w-full text-left px-4 py-3 hover:bg-white/10 transition-colors flex items-center">
                <i class="fas fa-heart mr-3 text-accent-300"></i>
                Favorites
              </button>
              <hr class="border-white/20 my-2">
              <button @click="handleLogout" class="w-full text-left px-4 py-3 hover:bg-white/10 transition-colors flex items-center text-red-300">
                <i class="fas fa-sign-out-alt mr-3"></i>
                Logout
              </button>
            </div>
          </div>

          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu" class="mobile-menu-button md:hidden p-3 rounded-full hover:bg-white/10 transition-all duration-300">
            <i class="fas fa-bars text-xl text-primary-300" :class="isMobileMenuOpen ? 'rotate-90' : ''"></i>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
      v-show="isMobileMenuOpen"
      class="md:hidden glass-effect border-t border-white/20 origin-top transform transition-all duration-300 ease-out"
      :class="isMobileMenuOpen ? 'scale-y-100 opacity-100' : 'scale-y-0 opacity-0'"
    >
      <div class="mobile-menu container mx-auto px-4 py-4">
        <button @click="navigateTo('/')" class="w-full py-4 px-4 rounded-xl hover:bg-white/10 flex items-center transition-all duration-300 group">
          <i class="fas fa-home mr-4 text-primary-300 w-6 text-center group-hover:text-primary-200"></i> 
          <span class="font-medium">Home</span>
        </button>
        <button @click="navigateTo('/about')" class="w-full py-4 px-4 rounded-xl hover:bg-white/10 flex items-center transition-all duration-300 group">
          <i class="fas fa-info-circle mr-4 text-primary-300 w-6 text-center group-hover:text-primary-200"></i> 
          <span class="font-medium">About</span>
        </button>
        <button @click="navigateTo('/services')" class="w-full py-4 px-4 rounded-xl hover:bg-white/10 flex items-center transition-all duration-300 group">
          <i class="fas fa-cogs mr-4 text-primary-300 w-6 text-center group-hover:text-primary-200"></i> 
          <span class="font-medium">Services</span>
        </button>
        <button @click="navigateTo('/contact')" class="w-full py-4 px-4 rounded-xl hover:bg-white/10 flex items-center transition-all duration-300 group">
          <i class="fas fa-envelope mr-4 text-primary-300 w-6 text-center group-hover:text-primary-200"></i> 
          <span class="font-medium">Contact</span>
        </button>
        
        <!-- Mobile CTA -->
        <div class="mt-4 pt-4 border-t border-white/20">
          <button @click="handleGetStarted" class="w-full bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-6 py-3 rounded-full font-medium transition-all duration-300 transform hover:scale-105">
            Get Started
          </button>
        </div>
      </div>
    </div>

    <!-- Search Overlay -->
    <div
      v-if="isSearchOpen"
      class="fixed inset-0 bg-black/80 backdrop-blur-sm flex items-center justify-center z-50 animate-fade-in"
      @click="toggleSearch"
    >
      <div class="glass-effect w-11/12 md:w-1/2 max-w-2xl rounded-2xl p-6 border border-white/20 shadow-2xl" @click.stop>
        <div class="flex items-center mb-4">
          <div class="flex-1 relative">
            <i class="fas fa-search absolute left-4 top-1/2 transform -translate-y-1/2 text-gray-400"></i>
            <input
              id="search-input"
              v-model="searchQuery"
              @keyup.enter="handleSearch"
              type="text"
              placeholder="Search for anything..."
              class="w-full pl-12 pr-4 py-4 bg-white/10 border border-white/20 rounded-xl outline-none text-white text-lg placeholder-gray-400 focus:border-primary-400 transition-colors"
            />
          </div>
          <button @click="toggleSearch" class="ml-4 p-2 text-gray-400 hover:text-white transition-colors">
            <i class="fas fa-times text-2xl"></i>
          </button>
        </div>
        
        <!-- Search Suggestions -->
        <div class="space-y-2">
          <div class="text-sm text-gray-400 mb-3">Popular searches:</div>
          <button @click="searchQuery = 'Web Development'; handleSearch()" class="block w-full text-left px-4 py-2 rounded-lg hover:bg-white/10 transition-colors text-gray-300">
            <i class="fas fa-laptop-code mr-2 text-primary-400"></i>
            Web Development
          </button>
          <button @click="searchQuery = 'UI/UX Design'; handleSearch()" class="block w-full text-left px-4 py-2 rounded-lg hover:bg-white/10 transition-colors text-gray-300">
            <i class="fas fa-paint-brush mr-2 text-accent-400"></i>
            UI/UX Design
          </button>
          <button @click="searchQuery = 'SEO Services'; handleSearch()" class="block w-full text-left px-4 py-2 rounded-lg hover:bg-white/10 transition-colors text-gray-300">
            <i class="fas fa-chart-line mr-2 text-secondary-400"></i>
            SEO Services
          </button>
        </div>
        
        <div class="mt-6 flex justify-end">
          <button @click="handleSearch" class="bg-gradient-to-r from-primary-500 to-secondary-500 hover:from-primary-600 hover:to-secondary-600 px-6 py-2 rounded-lg font-medium transition-all duration-300">
            Search
          </button>
        </div>
      </div>
    </div>
  </header>
</template>
