<template>
  <div
    class="bottom-0 sm:flex backImg w-full h-[207px] mt-20 justify-between items-center"
  >
    <div class="ml-12">
      <img class="w-40" src="/Asset 14.png" alt="" />
    </div>
    <div class="flex mr-12">
      <div class="md:mx-8 ml-12 md:ml-0" v-for="icon in icons">
        <img class="cursor-pointer w-10 h-10" :src="icon" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const icons = [
  "/icons/facebook.svg",
  "/icons/icons8-telegram.svg",
  "/icons/instagram.svg",
  "/icons/tiktok.svg",
];
</script>

<style scoped>
.backImg {
  background-image: url("/images/Bottom bar.png");
}
</style>
