<template>
  <div class="flex justify-center">
    <div class="mt-36 w-3/5 h-40 flex justify-center items-center">
      <h1 class="text-5xl font-splash text-black">Candidaphenome</h1>
      <router-link to="/devlog">
        <!-- Dynamically bind the latest version number -->
        <span class="rounded-3xl bg-black px-2 text-white">{{ latestVersion }}</span>
      </router-link>
    </div>
  </div>
</template>

<script>
import jsonData from '../assets/devlog.json';

export default {
  data() {
    return {
      latestVersion: jsonData[0].version,
    };
  },
};
</script>
