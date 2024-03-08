;
<template>
  <main>
    <div class="bg-blue-200 lg:overflow-hidden lg:pb-14 lg:pt-8">
      <div class="mx-auto max-w-7xl lg:px-8">
        <div class="lg:grid lg:grid-cols-2 lg:gap-8">
          <div class="mx-auto max-w-md px-6 sm:max-w-2xl sm:text-center lg:flex lg:items-center lg:px-0 lg:text-left">
            <div class="lg:py-24">
              <h1 class="text-8xl font-bold tracking-tight text-white sm:text-6xl lg:mt-6 xl:text-6xl">
                <span class="block text-8xl">Art Portfolio</span>
               
              </h1>
              
            </div>
          </div>
          <div class="-mb-16 mt-12 sm:-mb-48 lg:relative lg:m-0">
            <div class="mx-auto max-w-md px-6 sm:max-w-2xl lg:max-w-none lg:px-0">
              <!-- Illustration taken from Lucid Illustrations: https://lucid.pixsellz.io/ -->
              <img
                class="w-full lg:absolute lg:inset-y-0 lg:left-0 lg:h-full lg:w-auto lg:max-w-none"
                src="https://tailwindui.com/img/component-images/cloud-illustration-indigo-400.svg"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>

  <main>
    <a id="intro"></a>
    <div class="bg-white lg:overflow-hidden lg:pb-14 lg:pt-8">
      <div class="mx-auto max-w-7xl lg:px-8">
        <div class="lg:grid lg:grid-cols-2 lg:gap-8">
          <div class="mx-auto max-w-md px-6 sm:max-w-2xl sm:text-center lg:flex lg:items-center lg:px-0 lg:text-left">
            <div class="lg:py-24">
              <h1 class="text-2xl font-bold tracking-tight text-pink-400 sm:text-6xl lg:mt-6 xl:text-6xl">
                <span class="block">Introduction</span>
              </h1>
              <p class="mt-3 text-base text-blue-400 sm:mt-5 sm:text-xl lg:text-2xl xl:text-2xl">
               
               A journey to my canvas

           </p>
              <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">
               
                  I am Junoon , a passionate aspiring artist driven by the belief that art is powerful  language. My artistic journey mostly  began  in year 2020. Join me in this visual  odyssey  and see the world through my artistic lens.

              </p>
            </div>
          </div>
          <div class="-mb-16 mt-12 sm:-mb-48 lg:relative lg:m-0">
            <div class="mx-auto max-w-md px-6 sm:max-w-2xl lg:max-w-none lg:px-0">
              <!-- Illustration taken from Lucid Illustrations: https://lucid.pixsellz.io/ -->
              <img
                class="w-full lg:absolute lg:inset-y-0 lg:left-40 lg:top-5 lg:h-full lg:w-auto lg:max-w-none"
                src="../public/personalimg.jpg"
                alt=""
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
  <div class="bg-yellow-200">
    <a id="art"></a>
    <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <h2 class="sr-only">Art</h2>
      <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none pb-16">
        <h2 class="text-3xl font-bold tracking-tight text-pink-400 sm:text-4xl">My Art</h2>
      </div>
      <div class="grid grid-cols-1 gap-y-4 sm:grid-cols-2 sm:gap-x-6 sm:gap-y-10 lg:grid-cols-3 lg:gap-x-8">
        <div
          v-for="item in art"
          :key="item.id"
          class="group relative flex flex-col overflow-hidden rounded-lg border border-gray-200 bg-white"
        >
          <div class="aspect-h-4 aspect-w-3 bg-gray-200 sm:aspect-none group-hover:opacity-75 sm:h-96">
            <img
              :src="item.imageSrc"
              :alt="item.imageAlt"
              class="h-full w-full object-cover object-center sm:h-full sm:w-full"
            />
          </div>
          <div class="flex flex-1 flex-col space-y-2 p-4">
            <h3 class="text-sm font-medium text-gray-900">
              <NuxtLink
                :to="{
                  name: 'art-slug',
                  params: { slug: item.slug },
                }"
              >
                <span aria-hidden="true" class="absolute inset-0" />
                {{ item.name }}
              </NuxtLink>
            </h3>
            <p class="text-sm text-gray-500">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const art = [
  {
    id: 1,
    name: 'Watercolor',
    slug: 'Watercolor',
    description: 'With watercolor as my choosen medium , I created these works in 2023.',
    imageSrc: 'watercolor.jpg',
    imageAlt: 'Art piece 1 alt text.',
  },
  {
    id: 2,
    name: 'Oil Paintings',
    slug: 'Oil Paintings',
    description: 'With oilcolor as my choosen medium , I created these works in between 2020 and 2023..',
    imageSrc: 'oilpaintmain.jpg',
    imageAlt: 'Art piece 2 alt text.',
  },
  {
    id: 3,
    name: 'Acrylic Color',
    slug: 'Acrylic Color',
    description: 'With acrylics as my choosen medium , I created these works in 2023.',
    imageSrc: 'acrylicmain.jpg',
    imageAlt: 'Art piece 3 alt text.',
  },
  {
    id: 4,
    name: 'Charcoal Works',
    slug: 'Charcoal Works',
    description: 'With charcoal as my choosen medium , I created these works in 2023.',
    imageSrc: 'charcolemain.jpg',
    imageAlt: 'Art piece 4 alt text.',
  },
  {
    id: 5,
    name: 'Digital Works',
    slug: 'Digital Works',
    description: 'With digital arts as my choosen medium , I created these works in 2023.',
    imageSrc: 'https://placehold.co/400?text=Art+piece',
    imageAlt: 'Art piece 5 alt text.',
  },
  {
    id: 6,
    name: 'Photography Works',
    slug: 'Photography Works',
    description: 'Here are some photographs',
    imageSrc: 'https://placehold.co/400?text=Art+piece',
    imageAlt: 'Art piece 6 alt text.',
  },
]
</script>
