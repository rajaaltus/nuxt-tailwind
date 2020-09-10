<template>
  <div class="bg-gray-900">
    <div class="sm:container sm:mx-auto sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3">
      <div class="flex items-center px-4 py-3 justify-between sm:p-0">
        <div>
          <img class="h-10" src="/logo_apj.svg" alt="Logo APJ" />
        </div>

        <div class="sm:hidden">
          <button @click="isOpen = !isOpen" type="button" class="relative z-20 block text-gray-500 focus:outline-none hover:text-white">
            <svg class="fill-current h-8 w-8" viewBox="0 0 20 20">
              <path v-if="isOpen" d="M14 15h-1l-3-3-3 3a1 1 0 11-1-2l2-3-2-3a1 1 0 111-2l3 3 3-3a1 1 0 111 2l-2 3 2 3v2z" />
              <path v-if="!isOpen" d="M16 9H4l-1 1 1 1h12l1-1-1-1zm0 4H4l-1 1 1 1h12l1-1-1-1zM4 7h12l1-1-1-1H4L3 6l1 1z" />
            </svg>
          </button>
        </div>
      </div>

      <div :class="isOpen ? 'block' : 'hidden'" class="sm:block">
        <div class="px-2 pt-2 pb-4 sm:flex sm:items-center sm:p-0">
          <nuxt-link to="/login" class="block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2">List your property</nuxt-link>
          <nuxt-link to="/" class="mt-1 block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2">Trips</nuxt-link>
          <nuxt-link to="/" class="mt-1 block px-2 py-1 rounded text-white font-semibold hover:bg-gray-800 sm:mt-0 sm:ml-2">Messages</nuxt-link>
          <account-dropdown class="hidden sm:block sm:ml-6" />
        </div>
      
      
      <div class="px-4 py-5 border-t border-gray-800 sm:hidden">
        <div class="flex items-center">
          <img
            class="h-12 w-12 border-2 border-gray-600 rounded-full object-cover"
            src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
            alt="avatar"
          />
          <span class="text-white ml-3 font-semibold">Jane Doe</span>
        </div>
        <button class="fixed top-0 left-0 right-0 bottom-0 h-full w-full bg-black opacity-0 cursor-default"></button>
        <div class="mt-4">
          <a class="mt-2 block text-gray-400 hover:text-white" href="#">Account Settings</a>
          <a class="mt-2 block text-gray-400 hover:text-white" href="#">Support</a>
          <a class="mt-2 block text-gray-400 hover:text-white" href="#">Sign out</a>
        </div>
      </div>
    </div>
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
