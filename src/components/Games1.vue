<script setup lang="ts">
const games = [
  { imgSrc: "/assets/games/gametype.2813.jpg", name: "Double Jackpot", creator: "NetentGames" },
  { imgSrc: "/assets/games/gametype.4298.jpg", name: "All Aboard: Dynam...", creator: "RushGameStudio" },
  { imgSrc: "/assets/games/gametype.4749.jpg", name: "Book Of Tombs", creator: "NetentGames" },
  { imgSrc: "/assets/games/gametype.4779.jpg", name: "Rudolph’s Ride", creator: "NetentGames" },
  { imgSrc: "/assets/games/gametype.5423.jpg", name: "Starburst XXXtreme", creator: "StarBurst Inc." },
  { imgSrc: "/assets/games/gametype.1882.jpg", name: "Black Diamond", creator: "RushGameStudio" },
];
</script>

<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 mt-6">
    <!-- Game Card -->
    <div class="group hover:scale-105 text-left cursor-pointer" v-for="g in games">
      <img :src="g.imgSrc" class="rounded-xl" />
      <h3 class="font-bold mt-2 group-hover:text-[#4870FF]">{{ g.name }}</h3>
      <h4 class="text-xs opacity-50">{{ g.creator }}</h4>
    </div>
  </div>
</template>
