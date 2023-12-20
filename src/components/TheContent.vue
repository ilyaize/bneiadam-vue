<template>
  <!-- Hero section -->
  <div class="relative isolate overflow-hidden bg-gray-900 pb-16 pt-14 sm:pb-20">
    <img
      src="../assets/background.jpg"
      alt=""
      class="absolute inset-0 -z-10 h-full w-full object-cover"
    />
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl py-8 sm:py-12 lg:py-14">
        <div class="text-center">
          <h2 class="mt-6 text-3xl pb-12 leading-8 text-white">
            Welcome to <span class="font-bold text-yellow-500">Bnei Adam</span>
          </h2>
          <a href="https://youtu.be/dQw4w9WgXcQ">
            <img class="rounded-lg video-image" src="../assets/image.jpg" alt="" />
          </a>
          <h1 class="text-4xl pt-8 font-bold tracking-tight text-white sm:text-6xl">
            Holistic Medicine for <span class="text-yellow-500">Body and Mind</span>
          </h1>
          <p class="mt-6 text-lg leading-8 text-gray-300">
            Bnei Adam offers a unique approach to wellness, integrating the power of psychology and
            osteopathy to heal minds and restore bodies. Our compassionate team under the guidance
            of Michael Amar will help you find balance and vitality.
          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="tel:+972544619687"
              class="rounded-full bg-yellow-500 px-7 py-5 text-sm font-semibold text-white shadow-sm hover:bg-yellow-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-yellow-400"
              >Call Now (+972 54-461-9687)</a
            >
            <a class="" href="#"
              ><i class="fa-brands fa-whatsapp fa-2xl" style="color: white"></i
            ></a>
            <a class="" href="#"
              ><i class="fa-brands fa-facebook fa-2xl" style="color: white"></i
            ></a>
            <a class="" href="#"
              ><i class="fa-brands fa-x-twitter fa-2xl" style="color: white"></i
            ></a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Feature section -->
  <div class="mt-16 sm:mt-28">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-3xl sm:text-center">
        <h2 class="text-base font-semibold leading-7 text-yellow-600">
          Lorem ipsum dolor sit amet.
        </h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
          Dive deeper into our unique approach:
        </p>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          In our practice, we believe that the mind and body are intricately connected and that true
          healing requires addressing both. This is why we've chosen to integrate the power of
          psychology and osteopathy to treat the whole person, not just their symptoms.
        </p>
      </div>
    </div>
    <div class="relative overflow-hidden pt-16">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <img
          src="../assets/osteopathy.webp"
          alt="App screenshot"
          class="mb-[-12%] rounded-xl shadow-2xl ring-1 ring-gray-900/10"
          width="2432"
          height="1442"
        />
        <div class="relative" aria-hidden="true">
          <div class="absolute -inset-x-20 bottom-0 bg-gradient-to-t from-white pt-[7%]" />
        </div>
      </div>
    </div>
    <div class="mx-auto mt-16 max-w-7xl px-6 sm:mt-20 md:mt-24 lg:px-8">
      <dl
        class="mx-auto grid max-w-2xl grid-cols-1 gap-x-6 gap-y-10 text-base leading-7 text-gray-600 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:grid-cols-3 lg:gap-x-8 lg:gap-y-16"
      >
        <div v-for="feature in features" :key="feature.name" class="relative pl-9">
          <dt class="inline font-semibold text-gray-900">
            <component
              :is="feature.icon"
              class="absolute left-1 top-1 h-5 w-5 text-yellow-600"
              aria-hidden="true"
            />
            {{ feature.name }}
          </dt>
          {{ ' ' }}
          <dd class="inline">{{ feature.description }}</dd>
        </div>
      </dl>
    </div>
  </div>
</template>

<script setup>
import {
  ArrowPathIcon,
  CloudArrowUpIcon,
  Cog6ToothIcon,
  FingerPrintIcon,
  LockClosedIcon,
  ServerIcon
} from '@heroicons/vue/20/solid'
const features = [
  {
    name: 'Push to deploy.',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit aute id magna.',
    icon: CloudArrowUpIcon
  },
  {
    name: 'SSL certificates.',
    description:
      'Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.',
    icon: LockClosedIcon
  },
  {
    name: 'Simple queues.',
    description: 'Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus.',
    icon: ArrowPathIcon
  },
  {
    name: 'Advanced security.',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit aute id magna.',
    icon: FingerPrintIcon
  },
  {
    name: 'Powerful API.',
    description:
      'Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.',
    icon: Cog6ToothIcon
  },
  {
    name: 'Database backups.',
    description: 'Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus. ',
    icon: ServerIcon
  }
]
</script>

<style scoped>
.video-image {
  transition: filter 0.3s ease;
}

.video-image:hover {
  filter: brightness(1.2);
}
</style>
