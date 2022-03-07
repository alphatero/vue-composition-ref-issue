<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { ref, onMounted } from "@vue/runtime-core";
import HelloWorld from "./components/HelloWorld.vue";
// const InputRef1 = ref(null);
// const InputRef2 = ref(null);
// const InputRef3 = ref(null);
// const InputRef4 = ref(null);
const refs = ref([]);
onMounted(() => console.log(refs.value));
</script>

<template>
  <div class="text-center selection:bg-green-100">
    <img class="mx-auto mt-12 mb-8" alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld
      v-for="index in 4"
      :key="index"
      :ref="(el) => (refs[index] = el)"
      msg="Vite + Vue 3 + Tailwindcss v3"
    />
    <img
      class="mx-auto my-8"
      alt="powered-by"
      src="./assets/powered-by-vitawind-bright.png"
    />
  </div>
</template>

<style></style>
