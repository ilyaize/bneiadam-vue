<template>
  <!-- Hero section -->
  <div class="relative isolate overflow-hidden bg-gray-900 pb-16 pt-14 sm:pb-20">
    <img
      src="../assets/background.jpg"
      alt=""
      class="absolute inset-0 -z-10 h-full w-full object-cover"
    />
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl py-16 sm:py-24 lg:py-28">
        <div class="text-center">
          <a href="https://youtu.be/dQw4w9WgXcQ">
            <img class="rounded-lg video-image" src="../assets/image.jpg" alt="" />
          </a>
          <h2 class="mt-6 text-3xl pb-6 leading-8 text-white">
            Welcome to <span class="font-bold text-yellow-500">Bnei Adam</span>
          </h2>
          <h1 class="text-4xl font-bold tracking-tight text-white sm:text-6xl">
            Holistic Medicine for <span class="text-yellow-500">Body and Mind</span>
          </h1>
          <p class="mt-6 text-lg leading-8 text-gray-300">
            Bnei Adam offers a unique approach to wellness, integrating the power of psychology and
            osteopathy to heal minds and restore bodies. Our compassionate team under the guidance
            of Michael Amar will help you find balance and vitality.
          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="#"
              class="rounded-full bg-yellow-500 px-7 py-5 text-sm font-semibold text-white shadow-sm hover:bg-yellow-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-yellow-400"
              >Call Now</a
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

  <!-- Feature section -->
  <div class="mt-32 sm:mt-56">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl sm:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-600">Everything you need</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
          No server? No problem.
        </p>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis
          suscipit eaque, iste dolor cupiditate blanditiis.
        </p>
      </div>
    </div>
    <div class="relative overflow-hidden pt-16">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <img
          src="https://tailwindui.com/img/component-images/project-app-screenshot.png"
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
              class="absolute left-1 top-1 h-5 w-5 text-indigo-600"
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

<style>
.video-image {
  transition: filter 0.3s ease;
}

.video-image:hover {
  filter: brightness(1.2);
}
</style>
