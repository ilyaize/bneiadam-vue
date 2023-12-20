<template>
  <div class="bg-red-600">
    <nav class="container px-6 py-8 mx-auto md:flex md:justify-between md:items-center">
      <div class="flex items-center justify-between">
        logo
        <!-- Mobile menu button -->
        <div @click="toggleNav" class="flex md:hidden">
          <button
            type="button"
            class="text-gray-100 hover:text-gray-400 focus:outline-none focus:text-gray-400"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </button>
        </div>
      </div>

      <ul
        :class="showMenu ? 'flex' : 'hidden'"
        class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0"
      >
        <li class="text-gray-100 hover:text-indigo-400">Home</li>
        <li class="text-gray-100 hover:text-indigo-400">About</li>
        <li class="text-gray-100 hover:text-indigo-400">Contact Us</li>
      </ul>
    </nav>
  </div>
</template>
<script>
import { ref } from 'vue'
export default {
  setup() {
    let showMenu = ref(false)
    const toggleNav = () => (showMenu.value = !showMenu.value)
    return { showMenu, toggleNav }
  }
}
</script>
