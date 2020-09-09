<template>
  <div class="sm:max-w-sm max-w-full px-6 mb-4 py-4 sm:p-0 sm:mb-8">
    <div class="">
      <div v-if="loading" class="border border-gray-300 shadow rounded-lg sm:max-w-sm max-w-full px-6 mb-4 py-4 sm:p-0 sm:mb-8">
        <div class="animate-pulse flex space-x-4 h-64">
          <img class="h-full w-full object-cover" src="https://canadiansamaritansforafrica.org/wp-content/uploads/2020/06/placeholder.png" alt="" />
        </div>
      </div>

      <div v-else class="relative pb-5/6">
        <img class="h-64 w-full object-cover rounded-lg" :src="property.imageUrl" :alt="property.imageAlt" />
      </div>
      <div class="relative px-6 -mt-16 transform hover:scale-105 cursor-pointer transition ease-in duration-150">
        <div v-if="loading" class="animate-pulse bg-white rounded-lg px-4 h-32">
          <div class="pt-1 space-y-4">
            <div class="h-4 mt-6 bg-gray-400 rounded w-3/4"></div>
            <div class="h-4 bg-gray-400 rounded"></div>
            <div class="h-4 bg-gray-400 rounded w-5/6"></div>
          </div>
        </div>
        <div v-else class="bg-white p-6 rounded-lg shadow-lg">
          <div class="flex items-baseline">
            <span class="inline-block mr-2 bg-green-600 text-xs text-white px-2 uppercase font-semibold tracking-wide rounded-full">New</span>
            <div class="text-gray-600 text-xs uppercase tracking-wide">{{ property.beds }} beds &bull; {{ property.baths }} baths</div>
          </div>
          <h4 class="mt-1 font-semibold text-lg leading-tight truncate">
            {{ property.title }}
          </h4>
          <div class="mt-1">
            {{ property.formattedPrice }}
            <span class="text-gray-600 text-sm"> / wk</span>
          </div>
          <div class="mt-2 flex items-center">
            <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-green-600' : 'text-gray-400'" class="fill-current h-4 w-4" viewBox="0 0 20 20">
              <path d="M10 1l2 7h7l-5 4 1 7-5-4-5 4 1-7-5-4h7l2-7z" />
            </svg>
            <span class="text-gray-600 text-sm ml-2"> {{ property.reviewCount }} reviews</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["property"],
  data() {
    return { loading: true };
  },
  async mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 2000);
  },
};
</script>
