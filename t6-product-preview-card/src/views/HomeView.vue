<script setup lang="ts">
// Define the product data as an object
const product = {
  category: "Perfume",
  name: "Gabrielle Essence Eau De Parfum",
  description:
    "A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.",
  price: 149.99,
  oldPrice: 169.99,
  mobileImage: "/image-product-mobile.jpg",
  desktopImage: "/image-product-desktop.jpg",
  cartIcon: "/icon-cart.svg",
};
</script>

<template>
  <main class="flex items-center justify-center min-h-screen bg-[#f2ebe3] px-4">
    <div class="flex flex-col md:flex-row bg-white rounded-2xl shadow-lg overflow-hidden w-full max-w-md md:max-w-2xl">

      <!-- Image Section -->
      <div class="w-full md:w-1/2">
        <!-- Mobile Image -->
        <img :src="product.mobileImage" :alt="product.name" class="w-full h-full object-cover md:hidden">
        <!-- Desktop Image -->
        <img :src="product.desktopImage" :alt="product.name" class="w-full h-full object-cover hidden md:block">
      </div>

      <!-- Content -->
      <div class="flex flex-col justify-between p-6 md:w-1/2">
        <div>
          <p class="text-sm uppercase tracking-widest text-[#6c7289]">{{ product.category }}</p>
          <h1 class="text-4xl font-bold text-[#1b4133] mt-2 leading-tight">{{ product.name }}</h1>
          <p class="text-[#6c7289] text-md mt-3">
            {{ product.description }}
          </p>
        </div>

        <!-- Price Section -->
        <div class="flex items-center gap-4 mt-2">
          <span class="text-2xl font-bold text-[#3c8067]">${{ product.price }}</span>
          <span class="text-[#6c7289] line-through">${{ product.oldPrice }}</span>
        </div>

        <!-- Button -->
        <button
          class="flex items-center justify-center bg-[#3c8067] text-white py-3 px-2 w-full mt-4 rounded-lg font-semibold text-lg gap-2 transition hover:bg-[#1b4133]">
          <img :src="product.cartIcon" alt="Cart Icon" class="w-5 h-5">
          Add to Cart
        </button>

      </div>
    </div>
  </main>
</template>
