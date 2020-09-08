<template>
  <div class="bg-gray-900">
    <div
      class="sm:container sm:mx-auto sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3"
    >
      <div class="flex items-center px-4 py-3 justify-between sm:p-0">
        <div>
          <img class="h-10" src="/logo_apj.svg" alt="Logo APJ" />
        </div>
        
        <div class="sm:hidden">
          <button
            @click="isOpen = !isOpen"
            type="button"
            class="block text-gray-500 focus:outline-none hover:text-white"
          >
            <svg class="fill-current h-8 w-8" viewBox="0 0 20 20">
              <path
                v-if="isOpen"
                d="M14 15h-1l-3-3-3 3a1 1 0 11-1-2l2-3-2-3a1 1 0 111-2l3 3 3-3a1 1 0 111 2l-2 3 2 3v2z"
              />
              <path
                v-if="!isOpen"
                d="M16 9H4l-1 1 1 1h12l1-1-1-1zm0 4H4l-1 1 1 1h12l1-1-1-1zM4 7h12l1-1-1-1H4L3 6l1 1z"
              />
            </svg>
          </button>
        </div>
      </div>

      <div
        :class="isOpen ? 'block' : 'hidden'"
        class="px-2 pt-2 pb-4 transition ease-in duration-300 sm:flex sm:p-0"
      >
        <nuxt-link
          to="/"
          class="block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2"
          >List your property</nuxt-link
        >
        <nuxt-link
          to="/"
          class="mt-1 block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2"
          >Trips</nuxt-link
        >
        <nuxt-link
          to="/"
          class="mt-1 block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2"
          >Messages</nuxt-link
        >
      </div>
      <account-dropdown class="ml-6" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>
