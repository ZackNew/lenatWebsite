<template>
  <div>
    <!-- sm:h-[600px] md:h-[940px] min-w-full -->
    <img class="z-0 customPosition" src="/images/home background.jpg" alt="" />
    <div class="flex items-center md:pr-12 md:pl-32 px-12">
      <div class="mx-auto">
        <h1 class="text-6xl md:text-8xl font-bold my-8 text-[#2a6dad]">
          Lenat
        </h1>
        <p class="mt-12 text-2xl md:text-4xl font-semibold">
          Your journey to motherhood, guided by expert care!
        </p>
        <!-- google and app store -->
        <div
          class="md:flex md:bg-white px-2 py-3 justify-around mt-16 w-[80%] mb-5 md:mb-0"
        >
          <div
            class="flex items-center justify-center bg-[#1e4ed9] rounded w-full mx-1 mb-4 md:mb-0 py-1 sm:py-0"
          >
            <img class="w-7 h-7 mr-2" src="/playstore.svg" alt="" />
            <div>
              <p class="text-xs text-center text-white">GET IT ON</p>
              <p class="text-white font-semibold text-center">Google Play</p>
            </div>
          </div>
          <div
            class="flex items-center justify-center border rounded w-full mx-1 py-1 sm:py-0"
          >
            <img class="w-8 h-8 mr-2" src="/apple-icon.webp" alt="" />
            <div>
              <p class="text-xs text-center">Download on the</p>
              <p class="font-semibold text-center">App Store</p>
            </div>
          </div>
        </div>
      </div>
      <div class="flex justify-between hidden w-[50%] sm:block">
        <img
          class="w-auto max-h-[700px] w-[300px] mx-auto"
          src="/images/Phone.png"
          alt=""
        />
      </div>
    </div>
    <div class="w-full bg-[#23659c] py-6">
      <p class="text-center text-white font-semibold text-xl md:text-3xl">
        Unlock the path to the best parenting experience!
      </p>
    </div>
  </div>
</template>

<style scoped>
.customPosition {
  position: absolute;
  top: 0;
  z-index: -1;
  width: 100%;
  height: 100vh;
  object-fit: cover;
}
</style>
