<template>
  <div class="relative">
    <button @click="showDrop= !showDrop" class="block h-12 w-12 rounded-full overflow-hidden border-2 border-gray-600 focus:outline-none focus-border-white">
      <img class="h-full w-full object-cover" src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80" alt="avatar">
    </button>
    <button v-if="showDrop" @click="showDrop = false" class="fixed top-0 left-0 right-0 bottom-0 h-full w-full bg-black opacity-0 cursor-default"></button>
    <div v-if="showDrop" class="absolute top-auto right-0 mt-2 py-2 w-56 bg-white rounded-lg shadow-xl">
      <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="#">Account Settings</a>
      <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="#">Support</a>
      <a class="block px-4 py-2 text-gray-800 hover:bg-indigo-500 hover:text-white" href="#">Sign out</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showDrop: false
    }
  }
}
</script>