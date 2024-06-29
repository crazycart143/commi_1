<script>
export default {
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    }
  }
}
</script>

<template>
  <nav
    class="flex justify-between w-full fixed z-10 bg-[#0A0027] top-0 left-0 h-[100px] md:h-[120px] p-4 md:px-[60px]"
  >
    <div class="flex justify-start items-center lg:w-[400px]">
      <img src="../assets/logo.webp" width="125" height="125" alt="asd" class="w-[220px]" />
    </div>
    <div class="hidden md:flex justify-end items-center w-full">
      <ul
        class="flex md:gap-x-6 lg:gap-x-10 justify-center items-end uppercase text-white md:text-xs lg:text-base"
      >
        <li>
          <a href="/" class="focus:outline-none">Leaderboard</a>
        </li>
        <li>
          <a href="/" class="focus:outline-none">Challenge</a>
        </li>
        <li>
          <a href="/" class="text-[#C6A3FF] focus:outline-none">Know More</a>
        </li>
        <li>
          <a href="/" class="focus:outline-none">Profile</a>
        </li>
        <li>
          <a class="bg-[#FDD79F] text-black p-2 focus:outline-none">Logout</a>
        </li>
      </ul>
    </div>
    <div class="flex md:hidden justify-end items-center">
      <button @click="toggleMenu" class="focus:outline-none">
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="white"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          ></path>
        </svg>
      </button>
    </div>
    <div
      v-if="isMenuOpen"
      class="absolute top-[100px] left-0 w-full h-[280px] bg-[#0A0027] flex flex-col items-center md:hidden"
    >
      <ul class="flex flex-col gap-y-2 items-center w-full mt-4 text-white uppercase">
        <li class="w-full text-center py-2">
          <a href="/">Leaderboard</a>
        </li>
        <li class="w-full text-center py-2">
          <a href="/">Challenge</a>
        </li>
        <li class="w-full text-center py-2">
          <a href="/">Know More</a>
        </li>
        <li class="w-full text-center py-2">
          <a href="/">Profile</a>
        </li>
        <li class="w-full text-center py-2">
          <a class="">Logout</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
nav,
ul,
li,
a {
  font-family: 'Acme', sans-serif;
}
</style>
