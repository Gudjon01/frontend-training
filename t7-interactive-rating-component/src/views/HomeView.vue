<script setup lang="ts">
import { ref } from 'vue';

const selectedRating = ref<number | null>(null);
const isSubmitted = ref<boolean>(false);

const ratings = [1, 2, 3, 4, 5];

const handleRatingSelect = (rating: number) => {
  selectedRating.value = rating;
  console.log('selected: ', selectedRating.value);
};

const handleSubmitReview = () => {
  if (selectedRating.value !== null) {
    isSubmitted.value = true;
  }
};
</script>

<template>
  <main class="flex items-center justify-center bg-[#121417] h-screen">
    <div
      class="bg-gradient-to-b from-[#252d37] overflow-hidden to-[#121417] text-white rounded-2xl shadow-lg w-full max-w-sm p-6 md:p-8 transition-all">
      <Transition mode="out-in">
        <div v-if="!isSubmitted" key="rating">
          <div class="flex items-center justify-center rounded-full bg-gradient-to-b from-[#252d37] to-[#121417] w-10 h-10">
            <img src="/icon-star.svg" alt="Rating" class="w-5 h-5">
          </div>

          <h2 class="text-2xl font-bold mt-4">How did we do?</h2>
          <p class="text-sm text-gray-400 mt-2">
            Please let us know how we did with your support request.
            All feedback is appreciated to help us improve our offering!
          </p>

          <!-- Rating -->
          <div class="flex justify-between mt-6">
            <button v-for="rating in ratings" :key="rating" @click="handleRatingSelect(rating)" :class="[
              'flex items-center justify-center rounded-full text-white font-bold text-lg transition-all duration-200 w-12 h-12',
              selectedRating === rating ? 'bg-orange-500' : 'bg-[#959eac]'
            ]">
              {{ rating }}
            </button>
          </div>

          <!-- Submit button -->
          <button @click="handleSubmitReview"
            class="w-full bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 mt-6 rounded-full transition-all duration-300 disabled:bg-gray-600 disabled:cursor-not-allowed"
            :disabled="selectedRating === null">
            SUBMIT
          </button>
        </div>
        <div v-else key="thankyou" class="flex flex-col items-center text-center">
          <img src="/illustration-thank-you.svg" alt="Thank You Image" class="w-32">
          <p class="bg-[#262b30] text-orange-500 text-sm px-4 py-1 rounded-full mt-4">
            You selected {{ selectedRating }} out of 5
          </p>
          <h2 class="text-2xl font-bold mt-4">Thank you!</h2>
          <p class="text-sm text-gray-400 mt-2">
            We appreciate you taking the time to give a rating.
            If you ever need more support, don’t hesitate to get in touch!
          </p>
        </div>
      </Transition>
    </div>
  </main>
</template>

<style scoped>
/* Slide Animation (slide to left when leaving, slide in from right when entering) */
.v-enter-active, .v-leave-active {
  transition: transform 0.25s ease;
}
.v-enter-from {
  transform: translateX(100%);
}
.v-enter-to {
  transform: translateX(0);
}
.v-leave-from {
  transform: translateX(0);
}
.v-leave-to {
  transform: translateX(-100%);
}
</style>
