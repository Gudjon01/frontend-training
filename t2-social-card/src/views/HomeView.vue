<script setup lang="ts">
const links = [
  { name: "PerixAI", url: "https://perixai.com" },
  { name: "GitHub", url: "https://github.com" },
  { name: "YouTube", url: "https://youtube.com" },
  { name: "LinkedIn", url: "https://linkedin.com" },
  { name: "Instagram", url: "https://instagram.com" },
];
</script>

<template>
  <div class="flex items-center justify-center h-screen w-screen bg-[#141414] p-4">
    <div class="flex flex-col w-full max-w-sm bg-[#1f1f1f] text-white items-center justify-center p-6 rounded-lg shadow-lg">
      
      <!-- Profile Image -->
      <img src="/avatar-jessica.jpeg" alt="Jessica Randall" class="rounded-full size-32 mb-4">
      
      <!-- Name -->
      <h2 class="text-xl font-bold text-white">Jessica Randall</h2>
      
      <!-- Location -->
      <p class="text-[#c5f82a] font-semibold">London, United Kingdom</p>
      
      <!-- Bio -->
      <p class="text-gray-300 pt-4 text-center">"Front-end developer and avid reader."</p>

      <!-- Links (Use <a> for semantic correctness) -->
      <div class="flex flex-col w-full px-4 gap-4 mt-6">
        <a v-for="link in links" :key="link.name" :href="link.url" target="_blank" rel="noopener noreferrer"
          class="bg-[#333333] w-full py-3 rounded-lg font-semibold text-white text-center focus:ring-4 focus:ring-[#c5f82a] 
          hover:bg-[#c5f82a] hover:text-black transition-all outline-none">
          {{ link.name }}
        </a>
      </div>
    </div>
  </div>
</template>
