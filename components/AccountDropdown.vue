<template>
  <div class="relative">
    <button @click="showDrop= !showDrop" class="relative z-10 block h-12 w-12 rounded-full overflow-hidden border-2 border-gray-600 focus:outline-none focus-border-white">
      <img class="h-full w-full object-cover" src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80" alt="avatar">
    </button>
    <button v-if="showDrop" @click="showDrop = false" tabindex="-1" class="fixed inset-0 h-full w-full"></button>
    <div v-if="showDrop" class="absolute z-10 right-0 mt-2 py-2 w-56 bg-white rounded-lg shadow-xl">
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
  },
  mounted() {
    const handleEscape = (e) => {
      if (e.key === 'Esc' || e.key === 'Escape') {
        this.showDrop = false
      }
    }
    document.addEventListener('keydown', handleEscape);

    // this.$once('hook:beforeDestroy', ()=> {
    //   document.removeEventListener('keydown', handleEscape)
    // })
  }
}
</script>