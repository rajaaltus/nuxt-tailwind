<template>
    <div class="flex items-center mx-2 rounded-lg bg-white shadow-lg overflow-hidden transform hover:scale-105 cursor-pointer transition ease-in duration-150">
        <img
          class="h-32 w-32 flex-shrink-0 object-cover"
          :src="destination.imageUrl"
          :alt="destination.imageAlt"
        />
      <div class="px-6 py-4">
        <h3 class="text-lg font-semibold text-gray-800">{{destination.city}}</h3>
        <p class="text-gray-600">{{destination.averagePrice}} / Night average</p>
        <div class="mt-4">
          <a href="#" class="text-indigo-500 hover:text-indigo-400">Explore {{destination.propertyCount}} Properties</a>
        </div>
      </div>
    </div>
  
</template>

<script>
export default {
  props: ['destination']
}
</script>