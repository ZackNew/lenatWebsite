<template>
  <div class="z-50">
    <div
      class="flex justify-between my-4 md:items-center"
      :class="
        $route.path !== '/auth/signin' && $route.path !== '/auth/register'
          ? 'md:bg-gradient-to-r md:from-transparentGray-100 md:to-transparentGray-500 md:bg-no-repeat md:bg-center'
          : ''
      "
      style="background-size: 100% 50px"
    >
      <div class="md:pl-12 pl-4">
        <nuxt-link :to="'/'"
          ><img class="w-16 h-16 md:w-32 md:h-32 z-20" src="/Logo.svg" alt=""
        /></nuxt-link>
      </div>
      <div
        v-if="
          $route.path !== '/auth/signin' && $route.path !== '/auth/register'
        "
      >
        <div
          class="pr-4 md:pr-12 flex justify-between items-center hidden md:flex"
        >
          <ul class="flex justify-around mr-4">
            <li class="mx-8">
              <nuxt-link
                :to="'/'"
                :class="$route.path === '/' && 'bg-white py-[6px] px-4 rounded'"
                class="font-semibold"
              >
                Home
              </nuxt-link>
            </li>
            <li class="mx-8">
              <nuxt-link
                :to="'/about'"
                :class="
                  $route.path === '/about' && 'bg-white py-[6px] px-4 rounded'
                "
                class="font-semibold"
              >
                About
              </nuxt-link>
            </li>
            <li class="mx-8">
              <nuxt-link
                :to="'/contact'"
                :class="
                  $route.path === '/contact' && 'bg-white py-[6px] px-4 rounded'
                "
                class="font-semibold"
              >
                Contact
              </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="block md:hidden relative">
          <Icon
            v-if="isDropdownVisible"
            name="heroicons:x-mark"
            size="32px"
            class="mx-4 md:mx-20 text-[#23659c] cursor-pointer"
            @click="toggleDropDown()"
          />
          <Icon
            v-if="!isDropdownVisible"
            name="heroicons:queue-list-solid"
            size="32px"
            class="mx-4 md:mx-20 text-[#23659c] cursor-pointer"
            @click="toggleDropDown()"
          />
          <div
            class="bg-white rounded absolute bg-opacity-80 right-3 w-48"
            v-if="isDropdownVisible"
          >
            <ul>
              <li class="px-6 py-2 border-b hover:bg-gray-100">
                <nuxt-link :to="'/'">Home</nuxt-link>
              </li>
              <li class="px-6 py-2 border-b hover:bg-gray-100">
                <nuxt-link :to="'/about'">About</nuxt-link>
              </li>
              <li class="px-6 py-2 border-b hover:bg-gray-100">
                <nuxt-link :to="'/contact'">Contact</nuxt-link>
              </li>
              <li class="px-6 py-2 whitespace-nowrap"></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="hidden md:block mr-2">
        <nuxt-link :to="'/auth/signin'">
          <button
            class="text-white bg-gradient-to-r from-gray-600 to-cyan-900 rounded py-1 px-4 font-semibold whitespace-nowrap"
          >
            Doctors Sign in
          </button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const isDropdownVisible = ref(false);

const toggleDropDown = () => {
  isDropdownVisible.value = !isDropdownVisible.value;
};
</script>
