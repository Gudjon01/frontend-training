<template>
  <div class="flex items-center justify-center h-screen bg-[#f4d04e] px-4">
    <div class="flex flex-col w-full max-w-sm border border-black bg-white p-6 rounded-3xl 
                shadow-[8px_8px_0px_black]">

      <!-- Illustration -->
      <img class="rounded-lg" src="/illustration-article.svg" alt="illustration">

      <!-- Learning Tag -->
      <div class="flex justify-start items-start w-full mt-4">
        <div class="bg-[#f4d04e] px-3 py-1 rounded-md font-bold text-black text-sm">
          Learning
        </div>

      </div>

      <!-- Published Date -->
      <p class="font-semibold mb-4 mt-2">Published 21 Dec 2023</p>

      <!-- Article Title -->
      <h1 class="text-2xl font-bold">HTML & CSS foundations</h1>

      <!-- Description -->
      <p class="text-gray-800 font-sans">
        These languages are the backbone of every website, defining structure, content, and presentation.
      </p>


      <!-- Author Section -->
      <footer class="flex mt-4 gap-4 items-center">
        <img class="size-8 rounded-full" src="/image-avatar.webp" alt="Profile photo of Greg Hooper, the author">
        <p class="font-bold">Greg Hooper</p>
      </footer>

    </div>
  </div>
</template>
