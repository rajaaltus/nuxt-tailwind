<template>
  <div class="antialiased text-gray-900">
    <Hero />

    <div class="sm:max-w-xl lg:container mx-auto px-4 sm:px-0 py-8">
      <h2 class="text-xl text-gray-900">Popular Destinations</h2>
      <p class="text-gray-600">
        A selection of great work-friendly city will boost up your production.
      </p>
      <div class="container flex flex-wrap justify-items-stretch mt-4">
        <div
          class="mt-6 w-full lg:w-1/2 xl:w-1/3"
          v-for="(destination, index) in popularDestinations"
          :key="index"
        >
          <Package :destination="destination" />
        </div>
      </div>
    </div>

    <div class="bg-gray-200">
      <div class="sm:container sm:mx-auto px-4 py-8">
        <h3 class="text-xl text-gray-900">Featured Properties</h3>
        <p class="text-gray-600">
          Our verified featured properties will help you to find the right
          place!
        </p>
        <div class="mt-8 flex flex-wrap justify-between items-center">
          <PropertyCard :property="property[0]" />
          <PropertyCard :property="property[1]" />
          <PropertyCard :property="property[2]" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      popularDestinations: [
        {
          city: "Toronto",
          averagePrice: 120,
          propertyCount: 76,
          imageUrl:
            "https://images.unsplash.com/photo-1599082323832-2676eca28e86?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1778&q=80",
          imageAlt: "toronto Skyline",
        },
        {
          city: "Malibu",
          averagePrice: 215,
          propertyCount: 32,
          imageUrl:
            "https://images.unsplash.com/photo-1563862083992-df719afbcd03?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
          imageAlt: "malibu",
        },
        {
          city: "Chicago",
          averagePrice: 140,
          propertyCount: 87,
          imageUrl:
            "https://images.unsplash.com/photo-1598885511440-218a568ede3d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1696&q=80",
          imageAlt: "chicago",
        },
        {
          city: "Seattle",
          averagePrice: 140,
          propertyCount: 54,
          imageUrl:
            "https://images.unsplash.com/photo-1598642327181-c4ea0e55025b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1342&q=80",
          imageAlt: "Seattle",
        },
        {
          city: "Colorado",
          averagePrice: 132,
          propertyCount: 66,
          imageUrl:
            "https://images.unsplash.com/photo-1598845511224-75cd1ac5fd23?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1778&q=80",
          imageAlt: "colorado",
        },
        {
          city: "Darjling",
          averagePrice: 99,
          propertyCount: 244,
          imageUrl:
            "https://images.unsplash.com/photo-1599129194878-aae4bd2b779d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80",
          imageAlt: "colorado",
        },
      ],
      property: [
        {
          imageUrl:
            "https://images.unsplash.com/photo-1598769569837-0ebb3f625485?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1352&q=80",
          imageAlt: "Grand Place",
          beds: 3,
          baths: 2,
          title:
            "Modern home in the city center Modern home in the city center",
          priceInCents: 23500,
          formattedPrice: "$23,500",
          reviewCount: 23,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1599202937077-3f7cdc53f2e1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80",
          imageAlt: "Holiday Inn",
          beds: 2,
          baths: 2,
          title:
            "Luxury stay in the hot of the city. Feel like home in abroad.",
          priceInCents: 20520,
          formattedPrice: "$20,520",
          reviewCount: 65,
          rating: 4.5,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1598632022981-9426f46c6e97?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=697&q=80",
          imageAlt: "Green Box",
          beds: 3,
          baths: 2,
          title:
            "Modern home in the city center Modern home in the city center",
          priceInCents: 23500,
          formattedPrice: "$23,500",
          reviewCount: 64,
          rating: 3,
        },
      ],
    };
  },
};
</script>
