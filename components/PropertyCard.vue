<template>
  <div class="sm:max-w-sm max-w-full px-6 mb-4 py-4 sm:p-0 sm:mb-8">
    <div class="relative pb-5/6">
      <img
        class="h-64 w-full object-cover rounded-lg"
        :src="property.imageUrl"
        :alt="property.imageAlt"
      />
    </div>
    <div></div>
    <div class="relative px-6 -mt-16 transform hover:scale-105 cursor-pointer transition ease-in duration-150">
      <div class="bg-white p-6 rounded-lg shadow-lg">
        <div class="flex items-baseline">
          <span
            class="inline-block mr-2 bg-teal-500 text-xs text-white px-2 uppercase font-semibold tracking-wide rounded-full"
            >New</span
          >
          <div class="text-gray-600 text-xs uppercase tracking-wide">
            {{ property.beds }} beds &bull; {{ property.baths }} baths
          </div>
        </div>
        <h4 class="mt-1 font-semibold text-lg leading-tight truncate">
          {{ property.title }}
        </h4>
        <div class="mt-1">
          {{ property.formattedPrice }}
          <span class="text-gray-600 text-sm"> / wk</span>
        </div>
        <div class="mt-2 flex items-center">
          <svg
            v-for="i in 5"
            :key="i"
            :class="i <= property.rating ? 'text-teal-500' : 'text-gray-400'"
            class="fill-current h-4 w-4"
            viewBox="0 0 20 20"
          >
            <path d="M10 1l2 7h7l-5 4 1 7-5-4-5 4 1-7-5-4h7l2-7z" />
          </svg>
          <span class="text-gray-600 text-sm ml-2">
            {{ property.reviewCount }} reviews</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["property"],
};
</script>
