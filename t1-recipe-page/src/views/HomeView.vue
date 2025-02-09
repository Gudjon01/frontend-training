<script setup lang="ts">
</script>

<template>
  <div class="min-h-screen flex items-center justify-center p-4 sm:p-8 bg-[#f8f1e8]">
    <div class="bg-white p-6 sm:p-8 rounded-lg shadow-lg w-full max-w-md sm:max-w-lg md:max-w-4xl">
      <!-- Recipe Image -->
      <img src="../assets/images/image-omelette.jpeg" alt="omelette" class="rounded-lg w-full mb-6">

      <!-- Header -->
      <h1 class="text-3xl sm:text-4xl font-[young-serif]">Simple Omelette Recipe</h1>
      <p class="text-gray-600 mt-4 text-sm sm:text-base">
        An easy and quick dish, perfect for any meal. This classic omelette combines beaten eggs cooked
        to perfection, optionally filled with your choice of cheese, vegetables, or meats.
      </p>

      <!-- Preparation Time -->
      <div class="m-4 p-4 mt-6 rounded-lg bg-[#fff5fa]">
        <h4 class="text-xl sm:text-2xl font-bold text-[#7b284f]">Preparation Time</h4>
        <ul class="list-disc pt-4 pl-6 sm:pl-8 marker:text-[#7b284f] marker:text-lg sm:marker:text-xl">
          <li><strong>Total</strong>: Approximately 10 minutes</li>
          <li><strong>Preparation</strong>: 5 minutes</li>
          <li><strong>Cooking</strong>: 5 minutes</li>
        </ul>
      </div>

      <!-- Ingredients -->
      <div class="my-8">
        <h2 class="text-2xl sm:text-3xl font-semibold text-[#7d3c1b] font-[outfit]">Ingredients</h2>
        <ul class="list-disc pt-4 pl-6 sm:pl-8 marker:text-[#7b284f] marker:text-lg sm:marker:text-xl text-sm sm:text-base">
          <li>2-3 large eggs</li>
          <li>Salt, to taste</li>
          <li>Pepper, to taste</li>
          <li>1 tablespoon of butter or oil</li>
          <li>Optional fillings: cheese, diced vegetables, cooked meats, herbs</li>
        </ul>
      </div>

      <hr class="my-8">

      <!-- Instructions -->
      <div>
        <h2 class="text-2xl sm:text-3xl font-semibold text-[#7d3c1b] font-[outfit]">Instructions</h2>
        <ol class="my-4 list-decimal pl-6 sm:pl-8 space-y-2 marker:text-[#7d3c1b] marker:text-lg sm:marker:text-xl marker:font-semibold text-sm sm:text-base">
          <li><strong>Beat the eggs</strong>: In a bowl, beat the eggs with a pinch of salt and pepper until they are
            well mixed. You can add a tablespoon of water or milk for a fluffier texture.</li>
          <li><strong>Heat the pan</strong>: Place a non-stick frying pan over medium heat and add butter or oil.</li>
          <li><strong>Cook the omelette</strong>: Once the butter is melted and bubbling, pour in the eggs. Tilt the pan
            to ensure the eggs evenly coat the surface.</li>
          <li><strong>Add fillings (optional)</strong>: When the eggs begin to set at the edges but are still slightly
            runny in the middle, sprinkle your chosen fillings over one half of the omelette.</li>
          <li><strong>Fold and serve</strong>: As the omelette continues to cook, carefully lift one edge and fold it
            over the fillings. Let it cook for another minute, then slide it onto a plate.</li>
          <li><strong>Enjoy</strong>: Serve hot, with additional salt and pepper if needed.</li>
        </ol>
      </div>

      <hr class="my-8">

      <!-- Nutrition -->
      <div>
        <h2 class="text-2xl sm:text-3xl font-semibold text-[#7d3c1b] font-[outfit]">Nutrition</h2>
        <p class="mt-2 text-sm sm:text-base">The table below shows nutritional values per serving without the additional fillings.</p>
        <table class="w-full mt-4 border-t border-gray-300 text-sm sm:text-base">
          <tbody>
            <tr class="border-b border-gray-300">
              <td class="py-3 pl-2 sm:pl-4 font-semibold text-gray-700">Calories</td>
              <td class="py-3 font-extrabold text-[#7d3c1b] text-right">277kcal</td>
            </tr>
            <tr class="border-b border-gray-300">
              <td class="py-3 pl-2 sm:pl-4 font-semibold text-gray-700">Carbs</td>
              <td class="py-3 font-extrabold text-[#7d3c1b] text-right">0g</td>
            </tr>
            <tr class="border-b border-gray-300">
              <td class="py-3 pl-2 sm:pl-4 font-semibold text-gray-700">Protein</td>
              <td class="py-3 font-extrabold text-[#7d3c1b] text-right">20g</td>
            </tr>
            <tr>
              <td class="py-3 pl-2 sm:pl-4 font-semibold text-gray-700">Fat</td>
              <td class="py-3 font-extrabold text-[#7d3c1b] text-right">22g</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Base Heading Styles */
h1 {
  @apply text-3xl sm:text-4xl font-[young-serif];
}

h2 {
  @apply text-2xl sm:text-3xl font-semibold text-[#7d3c1b] font-[outfit];
}

/* Table Styling */
tr {
  @apply border-b border-gray-300;
}

td:first-child {
  @apply py-3 pl-2 sm:pl-4 font-semibold text-gray-700;
}

td:last-child {
  @apply py-3 font-extrabold text-[#7d3c1b] text-right;
}
</style>
