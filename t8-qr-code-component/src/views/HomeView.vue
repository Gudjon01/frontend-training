<script setup lang="ts">
import { ref } from 'vue';
import QrcodeVue from 'qrcode.vue';

// The URL that will be encoded in the QR code.
const qrValue = ref(
  "https://www.youtube.com/watch?v=dQw4w9WgXcQ&pp=ygUXbmV2ZXIgZ29ubmEgZ2l2ZSB5b3UgdXA%3D"
);
</script>

<template>
  <main
    class="flex items-center justify-center min-h-screen bg-gradient-to-r from-purple-300 via-pink-300 to-red-300 p-4">
    <!-- Card Container -->
    <div class="bg-white rounded-2xl shadow-2xl p-8 max-w-sm w-full text-center">
      <div
        class="mx-auto mb-4 size-fit px-4 py-4 flex items-center justify-center bg-gradient-to-br from-indigo-500 to-purple-500 rounded-full shadow-md">
        <span class="text-white font-bold text-xl">QR</span>
      </div>

      <!-- QR Code -->
      <QrcodeVue :value="qrValue" :size="220" class="mx-auto mb-6" />

      <!-- Title -->
      <h1 class="text-2xl font-bold text-gray-800 mb-2">Scan Me</h1>

      <!-- Description -->
      <p class="text-gray-600 text-sm">
        Scan this QR code to visit our website and discover more about our projects.
      </p>
    </div>
  </main>
</template>

<style scoped>
/* Additional styling if necessary */
</style>
