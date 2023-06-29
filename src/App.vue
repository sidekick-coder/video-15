<script setup>
import { ref } from 'vue'
import VSlideXTransition from './components/VSlideXTransition.vue'

const show = ref(true)
</script>
<template>
  <div class="flex h-screen w-screen items-center justify-center bg-gray-900">
    <div class="min-h-[300px] min-w-[500px] rounded bg-white p-5 text-center">
      <div class="flex h-[300px] w-full flex-col items-center justify-center">
        <button @click="show = !show" class="mb-4 rounded bg-teal-500 px-4 py-2 text-white">
          Start
        </button>

        <div class="min-h-[150px]">
          <v-slide-x-transition>
            <ul v-if="show" class="w-[150px] rounded border p-4 text-left shadow">
              <li>Item 1</li>
              <li>Item 2</li>
              <li>Item 3</li>
              <li>Item 4</li>
            </ul>
          </v-slide-x-transition>
        </div>
      </div>
    </div>
  </div>
</template>
