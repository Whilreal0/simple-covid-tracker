<template>
  <footer class="bg-gray-900 text-white py-4 ">
    <div class="container mx-auto text-center flex items-center justify-between">
      <p class="text-sm  w-full">Copyright © {{ currentYear }} Whilmer R</p>
      
    </div>
  </footer>
</template>

<script>
export default {
    computed: {
    currentYear() {
      return new Date().getFullYear()
    }
    }
};
</script>

<style>
</style>