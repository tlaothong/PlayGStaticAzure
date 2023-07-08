<template>
  <div>
    <h2>Animation</h2>

    <button type="button"
      @click="isOpen = true"
      class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800">
      Open</button>

    <Transition name="fade">
      <div v-if="isOpen"
        class="max-w-sm bg-green-400 border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
        <div class="p-5">
          <a href="#">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy technology
              acquisitions 2021</h5>
          </a>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Here are the biggest enterprise technology
            acquisitions of 2021 so far, in reverse chronological order.</p>
          <a href="#"
            @click.prevent="isOpen = false"
            class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Close
            <svg class="w-3.5 h-3.5 ml-2"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 14 10">
              <path stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M1 5h12m0 0L9 1m4 4L9 9" />
            </svg>
          </a>
        </div>
      </div>
    </Transition>

  </div>
</template>

<script setup lang="ts">
const isOpen = ref(false);
</script>

<style>
.fade-enter-from {
  opacity: 0;
  transform: translateY(-130px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(-130px);
}

.fade-enter-active,
.fade-leave-active {
  transition: all 0.7s ease;
}
</style>
