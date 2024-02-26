<template>
  <div class="bg-white px-8">
    <div
      class="pt-12 max-w-[1530px] mx-auto min-h-[50vh] lg:min-h-[60vh] xl:min-h-[70vh]"
    >
      <h3 class="font-bold text-4xl my-8">Our Services</h3>
      <div
        v-for="service in services"
        class="sm:grid grid-cols-12 items-center justify-between"
      >
        <div v-if="service.id === index" class="col-span-5">
          <img class="fade-in-out" :src="service.imagePath" alt="" />
        </div>
        <div
          v-if="service.id === index"
          class="sm:ml-12 sm:px-16 col-span-7 fade-in-out"
        >
          <h3 class="text-2xl my-4 font-bold">
            {{ service.title }}
          </h3>
          <p class="text-xl">{{ service.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const services = [
  {
    id: 0,
    imagePath: "/images/Marketplace.jpg",
    title: "Marketplace",
    description:
      "We want to make your parenthood journey as enjoyable as possible. That's why we have a marketplace dedicated to you, a place where you can find all the maternity and baby related products you need.",
  },
  {
    id: 1,
    imagePath: "/images/Doctor consultation.jpg",
    title: "Doctor consultation",
    description:
      "Having a baby should be a positive experience, so our main focus is to create a safe and comfortable enviroment for you to bring your baby in to the world and being bonding immediatley. We give 24/7 doctor consultation for all the questions and concerns you may have!",
  },
  {
    id: 2,
    imagePath: "/images/Content.jpg",
    title: "Content",
    description:
      "Localize curated pregnancy contents and facts specifically designed for you. Going through pregnancy phases, we know the different surprizes that may occur at each trimester. These contents will be a guide to what's coming next.",
  },
];

let index = ref(0);
const intervalId = ref();

function changeIndex() {
  if (index.value + 1 === 3) {
    index.value = 0;
    return;
  }
  index.value++;
}

onMounted(() => {
  intervalId.value = setInterval(changeIndex, 4000);
});
</script>

<style scoped>
@keyframes fade-inout {
  0% {
    opacity: 0%;
  }
  100% {
    opacity: 100%;
  }
}
.fade-in-out {
  animation: fade-inout 2s;
}
</style>
