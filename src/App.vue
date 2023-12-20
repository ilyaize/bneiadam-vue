<template>
  <div class="bg-purple-500">
    <!-- Header -->
    <header class="absolute inset-x-0 top-0 z-50 mx-auto max-w-7xl">
      <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Bnei Adam</span>
            <img class="h-16 w-auto" src="./assets/logo.svg" alt="" />
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
              class="dropdown-trigger inline-block px-6 py-3 text-white leading-tight rounded focus:outline-none focus:ring-0 transition duration-150 ease-in-out"
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
                    <img src="./assets/us.svg" alt="en" />
                    English</a
                  >
                </li>
                <li>
                  <a
                    href="#"
                    class="block py-2 px-4 hover:bg-gray-100 focus:bg-gray-100 outline-none"
                    @click="hide"
                  >
                    <img src="./assets/il.svg" alt="he" />
                    Hebrew</a
                  >
                </li>
                <li>
                  <a
                    href="#"
                    class="block py-2 px-4 hover:bg-gray-100 focus:bg-gray-100 outline-none"
                    @click="hide"
                  >
                    <img src="./assets/fr.svg" alt="fr" />

                    French</a
                  >
                </li>
              </ul>
            </template>
          </Dropdown>
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
              <img class="h-16 w-auto" src="./assets/logo.svg" alt="" />
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
              <div class="py-6">
                <a
                  href="#"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50"
                  >Log in</a
                >
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>

    <main>
      <!-- Hero section -->
      <div class="relative isolate overflow-hidden bg-gray-900 pb-16 pt-14 sm:pb-20">
        <img
          src="./assets/background.jpg"
          alt=""
          class="absolute inset-0 -z-10 h-full w-full object-cover"
        />
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div class="mx-auto max-w-2xl py-32 sm:py-48 lg:py-56">
            <div class="text-center">
              <h1 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">
                Holistic Medicine for Body and Mind
              </h1>
              <p class="mt-6 text-lg leading-8 text-gray-300">
                Bnei Adam offers a unique approach to wellness, integrating the power of psychology
                and osteopathy to heal minds and restore bodies. Our compassionate team under the
                guidance of Michael Amar will help you find balance and vitality.
              </p>
              <div class="mt-10 flex items-center justify-center gap-x-6">
                <a
                  href="#"
                  class="rounded-md bg-yellow-500 px-7 py-5 text-sm font-semibold text-white shadow-sm hover:bg-yellow-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-yellow-400"
                  >Call Now</a
                >
                <a href="#" class="text-sm font-semibold leading-6 text-white"
                  >Learn more <span aria-hidden="true">→</span></a
                >
              </div>
            </div>
          </div>
        </div>
        <div
          class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
          aria-hidden="true"
        >
          <div
            class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-20 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
            style="
              clip-path: polygon(
                74.1% 44.1%,
                100% 61.6%,
                97.5% 26.9%,
                85.5% 0.1%,
                80.7% 2%,
                72.5% 32.5%,
                60.2% 62.4%,
                52.4% 68.1%,
                47.5% 58.3%,
                45.2% 34.5%,
                27.5% 76.7%,
                0.1% 64.9%,
                17.9% 100%,
                27.6% 76.8%,
                76.1% 97.7%,
                74.1% 44.1%
              );
            "
          />
        </div>
      </div>
      <div class="bg-red-500" id="about">hello</div>
    </main>

    <!-- Footer -->
    <!-- <footer class="mt-32 bg-gray-900 sm:mt-56" aria-labelledby="footer-heading">
      <h2 id="footer-heading" class="sr-only">Footer</h2>
      <div class="mx-auto max-w-7xl px-6 py-16 sm:py-24 lg:px-8 lg:py-32">
        <div class="xl:grid xl:grid-cols-3 xl:gap-8">
          <img
            class="h-7"
            src="https://tailwindui.com/img/logos/mark.svg?color=yellow&shade=500"
            alt="Company name"
          />
          <div class="mt-16 grid grid-cols-2 gap-8 xl:col-span-2 xl:mt-0">
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold leading-6 text-white">Solutions</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.solutions" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{
                      item.name
                    }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold leading-6 text-white">Support</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.support" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{
                      item.name
                    }}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="md:grid md:grid-cols-2 md:gap-8">
              <div>
                <h3 class="text-sm font-semibold leading-6 text-white">Company</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.company" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{
                      item.name
                    }}</a>
                  </li>
                </ul>
              </div>
              <div class="mt-10 md:mt-0">
                <h3 class="text-sm font-semibold leading-6 text-white">Legal</h3>
                <ul role="list" class="mt-6 space-y-4">
                  <li v-for="item in footerNavigation.legal" :key="item.name">
                    <a :href="item.href" class="text-sm leading-6 text-gray-300 hover:text-white">{{
                      item.name
                    }}</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer> -->
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

import Dropdown from './components/Dropdown.vue'

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
