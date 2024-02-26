<template>
  <div>
    <!-- sm:h-[600px] md:h-[940px] min-w-full -->
    <img
      class="z-0 customPosition"
      src="/images/Contact background.jpg"
      alt=""
    />
    <div
      class="md:flex bg-white rounded-3xl w-[90%] md:w-[75%] mx-auto border border-gray-400 bg-opacity-60 md:py-20 md:px-12 py-10 px-6 items-center justify-between"
    >
      <div class="md:w-2/5 w-[80%] mr-16">
        <h3 class="text-lg font-semibold text-[#23659c]">
          Let us know how we can help
        </h3>
        <p class="md:text-lg md:mt-4 mt-2">
          We're here to help and answer any question you might have, We look
          forward to hearing from you! Please fill out the form, of use the
          contact information below.
        </p>
        <p class="md:text-lg md:mt-4 mt-2">tenkaratech@gmail.com</p>
        <p class="md:text-lg md:mt-4 mt-2">+251944317559</p>
        <p class="md:text-lg md:mt-4 mt-2">
          Iklas building, 2nd floor, office 2-14, 4 kilo, Addis Ababa, Ethiopia
        </p>
      </div>
      <div class="md:w-3/5 w-[80%]">
        <div>
          <h3 class="text-[#23659c] font-semibold md:text-xl mb-1 mt-4">
            Full Name
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
            Email
          </h3>
          <input
            class="border border-gray-400 rounded-lg md:rounded-xl w-full h-12 lg:h-16 focus:outline-none px-4 text-lg"
            id="email"
            name="email"
            type="email"
          />
        </div>
        <div>
          <h3 class="text-[#23659c] font-semibold md:text-xl mb-1 mt-4">
            Message
          </h3>
          <textarea
            class="border border-gray-400 rounded-lg md:rounded-xl w-full h-28 md:h-48 focus:outline-none p-4 text-lg"
            id="message"
            name="message"
            type="text"
          />
        </div>
        <div class="flex justify-around mt-8">
          <button
            class="px-8 py-2 bg-gradient-to-r from-gray-700 to-cyan-900 rounded text-white font-semibold"
          >
            Submit
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
