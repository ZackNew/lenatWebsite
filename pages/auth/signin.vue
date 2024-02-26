<template>
  <div>
    <!-- sm:h-[600px] md:h-[940px] min-w-full -->
    <img
      class="z-0 customPosition"
      src="/images/Doctor sign in background.jpg"
      alt=""
    />
    <div class="min-h-[60vh]">
      <div
        class="bg-white rounded-3xl w-[90%] md:w-[75%] mx-auto border border-gray-400 bg-opacity-80 md:py-32 md:px-12 py-10 px-6 items-center justify-between"
      >
        <div class="md:w-[60%] sm:w-[80%] w-[90%] mx-auto">
          <div>
            <h3 class="text-[#23659c] font-semibold md:text-xl mb-1 mt-4">
              User Name
            </h3>
            <input
              class="border border-gray-400 rounded-lg md:rounded-xl w-full h-12 lg:h-16 focus:outline-none px-4 text-lg"
              id="full-name"
              name="full-name"
              type="text"
            />
          </div>
          <div>
            <h3 class="text-[#23659c] font-semibold md:text-xl mb-1 mt-4">
              Password
            </h3>
            <input
              class="border border-gray-400 rounded-lg md:rounded-xl w-full h-12 lg:h-16 focus:outline-none px-4 text-lg"
              id="email"
              name="email"
              type="email"
            />
          </div>
          <p
            class="font-semibold text-right md:mt-4 mt-2 lg:text-base text-sm text-[#23659c]"
          >
            Create new account
          </p>
        </div>
        <div class="flex justify-around mt-8">
          <button
            class="px-8 py-2 bg-gradient-to-r from-gray-700 to-cyan-900 rounded text-white font-semibold"
          >
            Sign in
          </button>
        </div>
      </div>
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
