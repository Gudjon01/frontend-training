<script setup lang="ts">
const categories = [
  {
    "category": "Reaction",
    "score": 80,
    "icon": "/icon-reaction.svg",
    "color": "bg-[#ff5757]/10 text-[#ff5757]"
  },
  {
    "category": "Memory",
    "score": 92,
    "icon": "/icon-memory.svg",
    "color": "bg-[#ffb01f]/10 text-[#ffb01f]"
  },
  {
    "category": "Verbal",
    "score": 61,
    "icon": "/icon-verbal.svg",
    "color": "bg-[#00bd91]/10 text-[#00bd91]"
  },
  {
    "category": "Visual",
    "score": 72,
    "icon": "/icon-visual.svg",
    "color": "bg-[#1125d4]/10 text-[#1125d4]"
  }
]

</script>

<template>
  <div class="flex items-center justify-center h-screen bg-[#ebf1ff] px-4">
    <div class="flex flex-col md:flex-row bg-white w-full max-w-2xl rounded-3xl shadow-lg overflow-hidden">
      <!-- Left Section -->
      <div
        class="flex flex-col items-center rounded-b-3xl md:rounded-3xl md:w-1/2 text-center bg-gradient-to-b from-[#7857ff] to-[#2e2be9] text-white p-8">
        <h3 class="text-lg font-semibold opacity-80">Your Result</h3>

        <!-- Circle -->
        <div
          class="flex flex-col items-center justify-center bg-gradient-to-b from-[#4e21ca] to-[#5b45f6] rounded-full mt-4 size-48">
          <span class="text-6xl font-bold">76</span>
          <p class="opacity-80 mt-1 text-lg">of 100</p>
        </div>
        <h2 class="text-2xl font-bold mt-4">Great</h2>
        <p class="text-md opacity-75 mt-2 text-center">
          You scored higher than 65% of the people who have taken these tests.
        </p>
      </div>

      <!-- Right Section -->
      <div class="flex flex-col p-10 md:w-1/2">
        <h3 class="text-lg font-bold">Summary</h3>

        <div v-for="category in categories" :key="category.category"
          class="flex justify-between items-center p-4 rounded-lg mt-3" :class="category.color">
          <div class="flex items-center gap-2">
            <img :src="category.icon" :alt="category.category + ' icon'" class="w-6 h-6">
            <span class="font-medium"> {{ category.category }}</span>
          </div>
          <div>
            <span class="font-bold text-gray-700"> {{ category.score }}</span>
            <span class="text-gray-600"> / 100</span>
          </div>
        </div>
        <button
          class="mt-6 bg-gray-800 text-white py-3 rounded-full text-lg hover:bg-gray-700 transition-all">
          Continue
        </button>
      </div>
    </div>
  </div>
</template>
