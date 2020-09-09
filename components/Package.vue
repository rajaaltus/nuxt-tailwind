<template>
  <div>
    <div v-if="loading" class="border border-gray-300 shadow rounded-lg mx-2 p-4">
      <div class="animate-pulse flex space-x-4">
        <div class="rounded-full bg-gray-400 h-12 w-12"></div>
        <div class="flex-1 space-y-4 py-1">
          <div class="h-4 bg-gray-400 rounded w-3/4"></div>
          <div class="space-y-2">
            <div class="h-4 bg-gray-400 rounded"></div>
            <div class="h-4 bg-gray-400 rounded w-5/6"></div>
          </div>
        </div>
      </div>
    </div>
    <div v-else
      class="flex items-center mx-2 rounded-lg bg-white shadow-lg overflow-hidden transform hover:scale-105 cursor-pointer transition ease-in duration-150 hover:shadow-xl"
    >
      <img class="h-32 w-32 flex-shrink-0 object-cover" :src="destination.imageUrl" :alt="destination.imageAlt" />
      <div class="px-6 py-4">
        <h3 class="text-lg font-semibold text-gray-800">{{ destination.city }}</h3>
        <p class="text-gray-600">{{ destination.averagePrice }} / Night average</p>
        <div class="mt-4">
          <a href="#" class="text-green-800 hover:text-green-700">Explore {{ destination.propertyCount }} Properties</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["destination"],
  data() {
    return {
      loading: true,
    };
  },
  async mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 3000);
  },
};
</script>
