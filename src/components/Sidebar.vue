<template>
  <nav
    class="w-full sm:w-full md:w-96 h-screen bg-white fixed flex flex-col justify-between py-4 px-8 z-50"
  >
    <ul class="w-full flex flex-col justify-center gap-2">
      <RouterLink
        to="/"
        class="bg-blue-500 p-2 rounded-lg text-gray-300 font-medium hover:text-white flex items-center gap-2"
        ><i class="fa-solid fa-house"></i>Home</RouterLink
      >
      <RouterLink
        to="/delivery"
        class="bg-blue-500 p-2 rounded-lg text-gray-300 font-medium hover:text-white flex items-center gap-2"
      >
        <i class="fa-solid fa-truck"></i>Delivery</RouterLink
      >
      <RouterLink
        to="/analitycs"
        class="bg-blue-500 p-2 rounded-lg text-gray-300 font-medium hover:text-white flex items-center gap-2"
        ><i class="fa-solid fa-chart-line"></i>Analitycs</RouterLink
      >
    </ul>

    <RouterLink
      to="/"
      class="w-1/2 sm:w-28 self-center bg-yellow-400 rounded-tr-full"
    >
      <img src="../assets/imgs/logoPelientraga.png" alt="logo pelientrega" />
    </RouterLink>

    <button
      class="md:hidden absolute w-5 h-5 bg-yellow-400 bottom-8 left-7 p-8 rounded-full flex items-center justify-center drop-shadow-md"
      @click="showHideSidebar"
    >
      <i class="fa-solid fa-xmark text-white text-2xl"></i>
    </button>

    <button
      class="btnBar absolute w-4 h-screen right-0 top-0 bottom-0 bg-yellow-400 translate-x-full"
      @click="showHideSidebar(), swapIcons()"
    >
      <i class="fa-solid fa-angle-left"></i>
    </button>
  </nav>
</template>

<script setup>
import { RouterLink } from "vue-router";

let isShowing = true;

const showHideSidebar = () => {
  const sidebar = document.querySelector("nav");
  if (isShowing) {
    sidebar.style.transform = "translateX(-100%)";
    isShowing = false;
    return;
  }
  sidebar.style.transform = "translateX(0%)";
  isShowing = true;
};

const swapIcons = () => {
  const btn_icon = document.querySelector(".btnBar i");
  if (isShowing) {
    btn_icon.classList = "fa-solid fa-angle-left";
    return;
  }
  btn_icon.classList = "fa-solid fa-angle-right";
};
</script>
