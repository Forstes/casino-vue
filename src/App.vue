<script setup lang="ts">
import CreateAccountBlock from "@/components/CreateAccountBlock.vue";
import Preloader from "@/components/Preloader.vue";
import RegisterPopUp from "@/components/RegisterPopUp.vue";
import Games1 from "@/components/Games1.vue";
import { Bars3Icon } from "@heroicons/vue/24/solid";
import { onMounted, ref } from "vue";

const isLoading = ref(true);
const popUpShown = ref(false);

onMounted(() => {
  // Loading
  setTimeout(() => {
    isLoading.value = false;
    showPopUp();
  }, 2000);
});

function showPopUp() {
  setTimeout(() => {
    popUpShown.value = true;
  }, 1000);
}
</script>

<template>
  <Preloader v-if="isLoading" />
  <template v-else>
    <RegisterPopUp :is-open="popUpShown" @on-close="popUpShown = false" />

    <nav class="px-4 sm:px-12 md:px-32 xl:px-44 h-[72px] flex flex-wrap justify-between sm:justify-between items-center bg-[#01011F66]">
      <div class="flex items-center h-full">
        <img src="/assets/logo.svg" alt="Logo" width="48" height="48" class="hidden sm:block object-cover rounded mr-16" />

        <Bars3Icon class="w-8 h-8 lg:hidden" />

        <ul class="hidden lg:flex items-center space-x-6 h-full">
          <li class="nav-item h-full">
            <a href="#" class="hover-text">Games</a>
          </li>
          <li class="nav-item h-full">
            <a href="#" class="hover-text">Contact Us</a>
          </li>
          <li class="nav-item h-full">
            <a href="#" class="hover-text">Terms of Use</a>
          </li>
          <li class="nav-item h-full">
            <a href="#" class="hover-text">About</a>
          </li>
        </ul>
      </div>

      <div class="flex space-x-12">
        <button class="text-lg font-bold hover:brightness-75" @click="popUpShown = true">Sign up</button>
        <button class="gradient-btn w-[114px] h-[40px] rounded-lg hover:brightness-110 text-lg font-bold">Log in</button>
      </div>
    </nav>

    <div class="px-4 sm:px-12 lg:px-18 xl:px-44">
      <header class="text-center pt-16 px-4">
        <h1 class="text-4xl md:text-5xl font-extrabold mb-6">
          AWESOME HTML5 GAMES <br />
          - NO MONEY!
        </h1>
        <p class="text-xl md:text-3xl font-normal">
          Your Perfect Place To Get Some <br />
          Fun And Excitement
        </p>
        <div class="mt-8 flex flex-col sm:flex-row justify-center items-center sm:space-x-4 space-y-4 sm:space-y-0">
          <button class="py-2 w-[160px] h-[44px] border-2 border-white rounded-lg hover:brightness-75">Log In</button>
          <button class="py-2 w-[160px] h-[44px] rounded-lg gradient-btn hover:brightness-110">Play</button>
        </div>

        <div class="flex justify-center mt-16">
          <CreateAccountBlock />
        </div>
      </header>

      <!-- Games -->
      <section class="py-12 sm:py-16 text-center">
        <div class="flex justify-between items-end space-x-2">
          <div>
            <h2 class="text-left text-2xl md:text-4xl font-bold">Our Games</h2>
            <p class="text-left sm:text-base mt-1.5">Get Virtual Welcome bonus after Sign Up</p>
          </div>

          <a href="#" class="underline underline-offset-2 font-semibold text-base">All games</a>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 justify-items-center gap-4">
          <Games1 />

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-6">
            <!-- Game card -->
            <div class="bg-[url('/assets/games/DynamiteRichesMW_BigWin_385x190.jpeg')] bg-center bg-cover h-40 rounded-xl p-4 text-left hover:scale-105 cursor-pointer">
              <h2 class="text-left font-bold mb-1.5 leading-5">
                Dynamite Riches <br />
                Megaways
              </h2>
              <h3 class="text-left max-w-40 text-[10px] leading-3">Miners revealed a gain of €46,672 for Sandra M.! You too, dynamite the reels of the Red Tiger Daily Jackpot machines</h3>
              <button class="rounded-xl bg-[#4870FF] hover:brightness-75 px-3 py-2 text-[10px] leading-3 mt-3">Play now</button>
            </div>

            <!-- Game card -->
            <div class="bg-[url('/assets/games/GOTM_GatorGold_385x190.jpeg')] bg-center bg-cover h-40 rounded-xl p-4 text-left hover:scale-105 cursor-pointer">
              <h2 class="text-left font-bold mb-1.5 leading-5">
                Gator Gold Deluxe
                <br />
                Gigablox
              </h2>
              <h3 class="text-left max-w-40 text-[10px] leading-3">These swamps conceal many dangers but especially precious treasures. Will you be able to find them?</h3>
              <button class="rounded-xl bg-[#4870FF] hover:brightness-75 px-3 py-2 text-[10px] leading-3 mt-3">Play now</button>
            </div>

            <div class="sm:col-span-2 group hover:scale-105 text-left">
              <img src="/assets/banner_promo.jpeg" class="h-30 object-cover rounded-xl" />
              <div class="flex justify-between">
                <div>
                  <h3 class="font-bold mt-2 group-hover:text-[#4870FF] text-xs sm:text-base">Our deals are not to be missed</h3>
                  <h4 class="text-xs opacity-50">Discover a wide range of weekly promotions</h4>
                </div>
                <button class="rounded-xl bg-[#4870FF] hover:brightness-75 px-2 sm:px-8 text-[10px] leading-3 mt-3 font-semibold">Read more</button>
              </div>
            </div>
          </div>
        </div>

        <h2 class="text-sm text-left max-w-[655px] mt-6">* We don't offer opportunities to play for real money. Our games are free demo. All games were invented for entertainment purposes only and do not offer real money prizes.</h2>
      </section>

      <!-- Contact Us -->
      <section class="pt-4 flex justify-center lg:justify-between gap-8">
        <div>
          <div class="max-w-lg mx-auto text-center lg:text-left pb-20">
            <h2 class="text-3xl md:text-4xl font-bold mb-1.5">Contact Us</h2>
            <p class="mb-6">If you have some questions, send us a message</p>
            <form class="space-y-6">
              <input type="text" placeholder="Firstname" class="w-full p-4 h-11 rounded-lg border border-gray-700" />
              <input type="email" placeholder="Email Address" class="w-full p-4 h-11 rounded-lg border border-gray-700" />
              <textarea placeholder="Your message here..." class="w-full p-4 rounded-lg border border-gray-700 h-32"></textarea>
              <div class="flex justify-between flex-wrap gap-8">
                <div class="flex items-center">
                  <input type="checkbox" class="mr-2" />
                  <label class="text-white">I Accept The <span class="underline underline-offset-2">Privacy Policy</span></label>
                </div>
                <button class="mx-auto sm:mx-0 px-6 bg-pink-500 rounded-xl w-32 h-11 font-bold gradient-btn hover:brightness-110">Send</button>
              </div>
            </form>
          </div>
        </div>

        <img src="/assets/image.png" class="hidden lg:block" />
      </section>
    </div>

    <!-- Footer -->
    <footer class="py-6 text-center bg-[#01011F] px-4 sm:px-12 md:px-32">
      <div class="flex justify-center gap-4">
        <a href="#" class="hover:text-pink-500 text-sm sm:text-lg font-bold">Disclaimer</a>
        <span class="hidden sm:block text-lg font-bold">|</span>
        <a href="#" class="hover:text-pink-500 text-sm sm:text-lg font-bold">Privacy Policy</a>
        <span class="hidden sm:block text-lg font-bold">|</span>
        <a href="#" class="hover:text-pink-500 text-sm sm:text-lg font-bold">Terms of Conditions</a>
      </div>

      <p class="mt-4 text-sm max-w-5xl mx-auto">This site does not provide any form of online gambling and delivers information for entertainment and research purposes only. The games listed by Topwinningslots are intended for adult audience entertainment (underage visitors are restricted) and do not offer real money or prizes. Practicing online free games does not imply future success at 'real money' gambling.</p>

      <hr class="max-w-5xl mx-auto my-6" />

      <div class="max-w-5xl mx-auto flex flex-wrap justify-center sm:justify-between gap-4">
        <p class="text-sm">&copy; 2022 Your Website Name. All Rights Reserved.</p>

        <div class="flex gap-4">
          <a href="#" target="_blank">
            <i class="fab fa-twitter w-4"></i>
          </a>
          <a href="#" target="_blank">
            <i class="fab fa-facebook w-4"></i>
          </a>
          <a href="#" target="_blank">
            <i class="fab fa-instagram w-4"></i>
          </a>
        </div>
      </div>
    </footer>
  </template>
</template>

<style>
body {
  background-image: url("/assets/bg_hero.png"), url("/assets/bg_contact.jpg");
  background-position: center -400px, center center;
  background-size: contain, cover;
  background-repeat: no-repeat;
  color: white;
}

.gradient-btn {
  background: linear-gradient(265.48deg, #4870ff -5.06%, #fa00ff 94.87%);
  box-shadow: 0px 4px 16px 0px #8a61ff99;
}

.nav-item {
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
}

.hover-text {
  transition: color 0.1s ease-in-out, transform 0.1s ease-in-out;
}

.hover-text::before {
  content: "";
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 4px;
  border-radius: 4px 4px 0 0;
  background-image: linear-gradient(to right, #ff00ff, #00ffff);
  clip-path: polygon(0% 0%, 0% 100%, 100% 100%, 100% 0%);
  transform: translateX(-100%);
  transition: transform 0.1s ease-in-out;
}

.hover-text:hover::before {
  transform: translateX(0);
}
</style>
