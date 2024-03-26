<template>
  <div>
    <Hero />
    <Services />
    <DesignedForParents />
    <div class="bg-white py-4">
      <h3 class="ml-12 my-8 font-bold text-4xl">Download our app</h3>
      <div>
        <div
          class="md:flex px-12 md:px-2 justify-around mt-16 md:w-[80%] lg:w-[60%] mx-auto mb-5 md:mb-0"
        >
          <div
            class="flex items-center justify-center bg-[#1e4ed9] rounded w-full mx-1 mb-4 py-3 cursor-pointer"
            @click="redirectTo('playStore')"
          >
            <img class="w-7 h-7 mr-2" src="/playstore.svg" alt="" />
            <div>
              <p class="text-xs text-center text-white">GET IT ON</p>
              <p class="text-white font-semibold text-center">Google Play</p>
            </div>
          </div>
          <div
            class="flex items-center justify-center border rounded w-full mb-4 mx-1 py-3"
          >
            <img class="w-8 h-8 mr-2" src="/apple-icon.webp" alt="" />
            <div>
              <p class="text-xs text-center">Download on the</p>
              <p class="font-semibold text-center">App Store</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const redirectTo = (whereTo: string) => {
  window.open(
    "https://play.google.com/store/apps/details?id=com.lenat.lenat",
    "_black"
  );
};
</script>
