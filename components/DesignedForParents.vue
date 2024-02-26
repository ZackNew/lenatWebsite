<template>
  <div class="bg-white">
    <div class="bg-gray-400 py-3 backdrop-blur-lg bg-opacity-25">
      <h3 class="font-bold text-3xl text-center">Designed for parents</h3>
    </div>
    <div class="mb-12">
      <h3 class="ml-12 my-8 font-bold text-4xl">
        See what others say about us
      </h3>
      <Carousel
        class="mx-12"
        :value="pon"
        :numVisible="3"
        circular
        :autoplayInterval="3000"
        :responsiveOptions="responsiveOptions"
      >
        <template #item="slotProps">
          <div class="">
            <img class="mx-auto" :src="slotProps.data" alt="" />
          </div>
        </template>
        <template #previousicon
          ><Icon
            class="w-8 h-8 text-gray-600 opacity-25"
            name="heroicons:arrow-left-circle-16-solid"
        /></template>
        <template #nexticon
          ><Icon
            class="w-8 h-8 text-gray-600 opacity-25"
            name="heroicons:arrow-right-circle-16-solid"
        /></template>
      </Carousel>
    </div>
  </div>
</template>

<script setup lang="ts">
const pon = [
  "/images/test 1.png",
  "/images/test 2.png",
  "/images/test 3.png",
  "/images/test 4.png",
];
const responsiveOptions = ref([
  {
    breakpoint: "1400px",
    numVisible: 2,
    numScroll: 1,
  },
  {
    breakpoint: "1199px",
    numVisible: 3,
    numScroll: 1,
  },
  {
    breakpoint: "767px",
    numVisible: 2,
    numScroll: 1,
  },
  {
    breakpoint: "575px",
    numVisible: 1,
    numScroll: 1,
  },
]);
</script>
