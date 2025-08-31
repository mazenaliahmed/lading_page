<script setup lang="ts">
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)
const isSearchOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const toggleSearch = () => {
  isSearchOpen.value = !isSearchOpen.value
}
</script>

<template>
  <header class="sticky top-0 z-50 bg-gradient-to-r from-gray-800 to-gray-900 text-white shadow-lg">
    <div class="container mx-auto px-4">
      <div class="flex items-center justify-between h-16">
        <!-- Logo -->
        <div class="flex items-center space-x-2">
          <i class="fas fa-rocket text-blue-400 text-2xl"></i>
          <span class="text-xl font-bold">BrandName</span>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center space-x-1">
          <a href="#" class="px-4 py-2 flex items-center rounded-md hover:bg-gray-700 transition">
            <i class="fas fa-home mr-2 text-blue-300"></i> Home
          </a>
          <a href="#" class="px-4 py-2 flex items-center rounded-md hover:bg-gray-700 transition">
            <i class="fas fa-info-circle mr-2 text-blue-300"></i> About
          </a>
          <a href="#" class="px-4 py-2 flex items-center rounded-md hover:bg-gray-700 transition">
            <i class="fas fa-cogs mr-2 text-blue-300"></i> Services
          </a>
          <a href="#" class="px-4 py-2 flex items-center rounded-md hover:bg-gray-700 transition">
            <i class="fas fa-envelope mr-2 text-blue-300"></i> Contact
          </a>
        </nav>

        <!-- Right Section -->
        <div class="flex items-center space-x-4">
          <!-- Search Icon -->
          <button @click="toggleSearch" class="p-2 rounded-full hover:bg-gray-700">
            <i class="fas fa-search"></i>
          </button>

          <!-- Profile -->
          <div class="hidden md:flex items-center space-x-2 cursor-pointer hover:bg-gray-700 p-2 rounded-lg">
            <div class="bg-blue-500 rounded-full w-8 h-8 flex items-center justify-center">
              <i class="fas fa-user"></i>
            </div>
            <span>John Doe</span>
          </div>

          <!-- Mobile Menu Button -->
          <button @click="toggleMobileMenu" class="md:hidden p-2 rounded-md hover:bg-gray-700">
            <i class="fas fa-bars text-xl"></i>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
      v-show="isMobileMenuOpen"
      class="md:hidden bg-gray-800 origin-top transform transition-all duration-300 ease-out"
      :class="isMobileMenuOpen ? 'scale-y-100 opacity-100' : 'scale-y-0 opacity-0'"
    >
      <div class="container mx-auto px-4 py-3">
        <a href="#" class="py-3 px-2 rounded-md hover:bg-gray-700 flex items-center transition">
          <i class="fas fa-home mr-3 text-blue-300 w-6 text-center"></i> Home
        </a>
        <a href="#" class="py-3 px-2 rounded-md hover:bg-gray-700 flex items-center transition">
          <i class="fas fa-info-circle mr-3 text-blue-300 w-6 text-center"></i> About
        </a>
        <a href="#" class="py-3 px-2 rounded-md hover:bg-gray-700 flex items-center transition">
          <i class="fas fa-cogs mr-3 text-blue-300 w-6 text-center"></i> Services
        </a>
        <a href="#" class="py-3 px-2 rounded-md hover:bg-gray-700 flex items-center transition">
          <i class="fas fa-envelope mr-3 text-blue-300 w-6 text-center"></i> Contact
        </a>
      </div>
    </div>

    <!-- Search Overlay -->
    <div
      v-if="isSearchOpen"
      class="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50"
    >
      <div class="bg-white w-11/12 md:w-1/2 rounded-lg p-4">
        <div class="flex items-center">
          <input
            type="text"
            placeholder="Search..."
            class="flex-1 border-none outline-none text-gray-900 text-lg p-2"
          />
          <button @click="toggleSearch" class="ml-2 text-gray-500 hover:text-gray-800">
            <i class="fas fa-times text-2xl"></i>
          </button>
        </div>
      </div>
    </div>
  </header>
</template>
