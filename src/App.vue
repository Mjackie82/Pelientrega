<template>
  <main class="w-full h-screen bg-indigo-50">
    <Sidebar />

    <RouterView class="ml-4" />
  </main>
</template>

<script setup>
import { RouterLink, RouterView } from "vue-router";
import Sidebar from "./components/Sidebar.vue";
</script>
