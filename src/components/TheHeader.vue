<template>
  <!-- Header -->
  <header class="absolute inset-x-0 top-0 z-50 mx-auto max-w-7xl">
    <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
      <div class="flex lg:flex-1">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">Bnei Adam</span>
          <img class="h-16 w-auto" src="../assets/logo.svg" alt="" />
        </a>
      </div>
      <div class="flex lg:hidden">
        <button
          type="button"
          class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-400"
          @click="mobileMenuOpen = true"
        >
          <span class="sr-only">Open main menu</span>
          <Bars3Icon class="h-16 w-16" aria-hidden="true" />
        </button>
      </div>
      <div class="hidden lg:flex lg:gap-x-12">
        <a
          v-for="item in navigation"
          :key="item.name"
          :href="item.href"
          class="text-sm font-semibold leading-6 text-white"
          >{{ item.name }}</a
        >
      </div>

      <div class="hidden lg:flex lg:flex-1 lg:justify-end">
        <Dropdown class="inline" popper-class=" bg-white border rounded-lg shadow-md px-4">
          <!-- Dropdown trigger -->
          <button
            class="dropdown-trigger inline-block px-12 py-6 text-white leading-tight rounded focus:outline-none focus:ring-0 transition duration-150 ease-in-out"
          >
            Lang
          </button>

          <!-- Dropdown content -->
          <template #popper="{ hide }">
            <ul class="py-1 text-gray-70">
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 hover:bg-gray-100 focus:bg-gray-100 outline-none"
                  @click="hide"
                >
                  <img src="../assets/us.svg" alt="en" />
                  English</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 hover:bg-gray-100 focus:bg-gray-100 outline-none"
                  @click="hide"
                >
                  <img src="../assets/il.svg" alt="he" />
                  Hebrew</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 hover:bg-gray-100 focus:bg-gray-100 outline-none"
                  @click="hide"
                >
                  <img src="../assets/fr.svg" alt="fr" />

                  French</a
                >
              </li>
            </ul>
          </template>
        </Dropdown>
        <a
          href="tel:+972544619687"
          class="rounded-full bg-yellow-500 px-7 py-6 text-sm font-semibold text-white shadow-sm hover:bg-yellow-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-yellow-400"
          >Call Now (+972 54-461-9687)</a
        >
      </div>
    </nav>
    <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
      <div class="fixed inset-0 z-50" />
      <DialogPanel
        class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
      >
        <div class="flex items-center justify-between">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Bnei Adam</span>
            <img class="h-16 w-auto" src="../assets/logo.svg" alt="" />
          </a>
          <button
            type="button"
            class="-m-2.5 rounded-md p-2.5 text-gray-700"
            @click="mobileMenuOpen = false"
          >
            <span class="sr-only">Close menu</span>
            <XMarkIcon class="h-16 w-16" aria-hidden="true" />
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/10">
            <div class="space-y-2 py-6">
              <a
                v-for="item in navigation"
                :key="item.name"
                :href="item.href"
                class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                >{{ item.name }}</a
              >
            </div>
          </div>
        </div>
      </DialogPanel>
    </Dialog>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

import Dropdown from './Dropdown.vue'

const navigation = [
  { name: 'Home', href: '#' },
  { name: 'About', href: '#about' },
  { name: 'Contact', href: '#contact' }
]

const mobileMenuOpen = ref(false)
</script>

<style scoped>
.dropdown-trigger::after {
  display: inline-block;
  margin-left: 0.255em;
  vertical-align: 0.255em;
  content: '';
  border-top: 0.3em solid;
  border-right: 0.3em solid transparent;
  border-bottom: 0;
  border-left: 0.3em solid transparent;
}
</style>
