<script setup lang="ts">
import { ref } from "vue";

const items = ref([
  {
    title: "What is Vue.js?",
    content: "Vue.js is a progressive JavaScript framework for building user interfaces.",
    open: false,
  },
  {
    title: "How does Vue 3 differ from Vue 2?",
    content: "Vue 3 introduces the Composition API, improved performance, and better TypeScript support.",
    open: false,
  },
  {
    title: "Is Vue good for large applications?",
    content: "Yes! Vue can scale well with modular architecture and Vuex or Pinia for state management.",
    open: false,
  },
]);

const toggleItem = (index: number) => {
  items.value[index].open = !items.value[index].open;
};
</script>

<template>
  <div class="flex items-center justify-center h-screen bg-[#f9f0ff] px-4">
    <div class="flex flex-col bg-white w-full max-w-sm p-6 rounded-lg shadow-lg">
      
      <!-- Header -->
      <div class="flex items-center justify-start gap-4">
        <img src="/icon-star.svg" alt="star icon">
        <h1 class="font-bold text-4xl">FAQs</h1>
      </div>

      <!-- Accordion Section -->
      <div class="mt-6">
        <div v-for="(item, index) in items" :key="index" class="border-b border-gray-300">
          
          <!-- Title -->
          <button @click="toggleItem(index)" class="flex justify-between items-center w-full py-3 text-left font-semibold text-gray-900 focus:outline-none">
            {{ item.title }}
            <img :src="item.open ? '/icon-minus.svg' : '/icon-plus.svg'" alt="Toggle Icon" class="size-5 transition-transform duration-300">
          </button>

          <!-- Content with Vue Transition -->
          <Transition name="accordion">
            <div v-if="item.open" class="overflow-hidden">
              <p class="text-gray-700 pb-3 pl-4">{{ item.content }}</p>
            </div>
          </Transition>
          
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped>
.accordion-enter-active, .accordion-leave-active {
  transition: max-height 0.3s ease-in-out, opacity 0.3s ease-in-out;
}

.accordion-enter-from, .accordion-leave-to {
  max-height: 0;
  opacity: 0;
}

.accordion-enter-to, .accordion-leave-from {
  max-height: 200px;
  opacity: 1;
}
</style>
