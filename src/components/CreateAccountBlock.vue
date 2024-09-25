<template>
  <div class="create-acc-block p-6 min-w-[320px] sm:min-w-[460px] w-min backdrop-blur rounded-3xl">
    <div class="flex flex-wrap justify-center lg:justify-between font-semibold text-center space-y-4 lg:space-y-0">
      <p class="text-[22px] font-bold uppercase">Create a Free Account Now</p>
      <ul class="flex justify-center flex-wrap space-x-4">
        <li class="flex items-center">
          <img src="/assets/icons/dice.png" alt="Icon" width="36" height="36" class="mr-2" />
          <span class="text-xs text-left"
            >1000+ Games <br />
            Available</span
          >
        </li>
        <li class="flex items-center">
          <img src="/assets/icons/slot.png" alt="Icon" width="36" height="36" class="mr-2" />
          <span class="text-xs text-left"
            >New Game <br />
            Every week</span
          >
        </li>
        <li class="flex items-center mt-3 md:mt-0">
          <img src="/assets/icons/24h.png" alt="Icon" width="36" height="36" class="mr-2" />
          <span class="text-xs text-left"
            >Support Our <br />
            Users 24/7</span
          >
        </li>
      </ul>
    </div>

    <form class="flex flex-col 2xl:flex-row space-x-4 space-y-6 lg:space-y-0 mt-4 items-center 2xl:items-start mt-8 lg:mt-4">
      <div>
        <div class="flex flex-col lg:flex-row space-y-4 lg:space-y-0 lg:space-x-4 justify-center">
          <input type="text" placeholder="Firstname" class="h-[44px] px-4 text-black text-base rounded-lg border border-gray-600" />
          <input type="text" placeholder="Lastname" class="h-[44px] px-4 text-black text-base rounded-lg border border-gray-600" />
          <input type="email" placeholder="Email Address" class="h-[44px] px-4 text-black text-base rounded-lg border border-gray-600" />
        </div>
        <div class="mt-3 flex items-center w-full">
          <input type="checkbox" class="mr-2" />
          <label class="text-white">I Accept The Privacy Policy</label>
        </div>
      </div>
      <button class="gradient-btn w-[160px] h-[44px] rounded-lg hover:brightness-110 text-lg font-bold">Join Now</button>
    </form>
  </div>
</template>

<style scoped>
.create-acc-block {
  background: linear-gradient(268.31deg, rgba(79, 89, 124, 0.4) 0%, rgba(123, 135, 175, 0.4) 50.52%, rgba(63, 72, 105, 0.4) 100%);
}
</style>
