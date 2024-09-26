<script setup lang="ts">
const props = defineProps({
  isOpen: Boolean,
});
const emit = defineEmits(["onClose"]);

function onClose() {
  emit("onClose");
}
</script>

<template>
  <div v-if="isOpen" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50" @click.self="onClose">
    <div class="bg-stone-700 opacity-95 p-6 rounded-lg shadow-lg w-96">
      <h2 class="text-xl font-bold mb-4">Register</h2>
      <form>
        <input type="text" placeholder="Firstname" class="w-full p-4 h-11 rounded-lg border border-gray-700" />
        <input type="email" placeholder="Email Address" class="w-full p-4 h-11 rounded-lg border border-gray-700 my-4" />
        <input type="password" placeholder="Password" class="w-full p-4 h-11 rounded-lg border border-gray-700" />
        <div class="flex justify-end mt-6">
          <button type="button" @click="onClose" class="mr-2 text-gray-500 mr-4">Cancel</button>
          <button type="submit" class="bg-blue-500 text-white rounded px-4 py-2 gradient-btn mt">Register</button>
        </div>
      </form>
    </div>
  </div>
</template>
