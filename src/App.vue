<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import About from './components/About.vue'
import Features from './components/Features.vue'
import Liner from './components/Top.vue'
import Map from './components/Map.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
function m() {
  const menu = document.querySelector("#menu")
  menu.classList.toggle("active")
}
</script>

<template>
  <div class="head">
    <!--mob-->
    <nav
      class="nav bg-gray-500 bg-transparent text-gray-200 md:hidde sticky top-0 z-10 justify-between font-semibold mobile">
      <div class="flex justify-between">
        <a href="https://pactel.info" onclick=""> <img src="/logo.svg" width="80" height="60" class="justify-between m-4"
            alt="logo"></a>
        <!-- <h1 style="font-weight: 800;" class="p-3 text-3xl text-gray-300">Courses</h1> -->
        <button @click="m" id="menub" class="md:hidde justify-between hover:bg-transparent">
          <div class="container dark:invert px-4">
            <div class="bar1">
              <hr class="border-2 bg-black border-black">
            </div>
            <!-- <div class="bar2">
              <hr class="border-2 bg-black border-black">
            </div> -->
            <div class="bar3">
              <hr class="border-2 bg-black border-black">
            </div>
          </div>
        </button>
      </div>
      <div class=" flex justify-center">
        <div
          class="menu notactive space-y-3 bg-gray-600 text-xl font-semibold transform bg-transparent text-gray-300 transition ease-in duration-500 bg-gray-00 "
          id="menu">
          <RouterLink to="/" @click="m"><a href="#" class="block -mb-6">Home</a></RouterLink>
          <!-- <hr class="border-1 rounded border-gray-400 m- opacity-50 "> -->
          <RouterLink to="/" @click="m" id="menub" class="block p-2">Our Services</RouterLink>
          <RouterLink to="/" @click="m" id="menub" class="block p-2">Construction Programs</RouterLink>
          <RouterLink to="/" @click="m" id="menub" class="block p-2">Cost Calculator</RouterLink>
          <a href="#" @click="m" class="block p-4 bg-blue-800 font-medium w-full">Contact</a>
        </div>
      </div>
    </nav>

    <!---->
    <RouterView />
    <!-- <div class="bar"></div> -->
    <header class=" flex justify-center space-x-20 text-black bg-gray-200 hiddenm desktop">
      <div class="flex justify-start">
        <div class="flex justify-start mr-96"><img alt="logo" class="logo -m-5" width="160" height="100" src="/logo.svg">
        </div>

        <div class="my-auto">

          <nav class="text-xl font-semibold flex justify-end space-x-8">
            <RouterLink to="/" active-class="text-blue-800" class="hover:text-blue-800">Home<div
                class="bg-blue-700 mx-auto mt-1 rounded-full">
              </div>
            </RouterLink>
            <RouterLink to="/about" active-class="text-blue-800" class="hover:text-blue-800">Our Services<div
                class="bg-blue-700 mx-auto mt-1 rounded-full"></div>
            </RouterLink>
            <RouterLink to="/2" active-class="text-blue-800" class="hover:text-blue-800">Construction Programs<div
                class="bg-blue-700 mx-auto mt-1 rounded-full"></div>
            </RouterLink>
            <RouterLink to="/3" active-class="text-blue-800" class="hover:text-blue-800">Cost Calculator<div
                class="bg-blue-700"></div>
            </RouterLink>
            <button href="#" class="px-5 bg-blue-600 text-white font-medium rounded-full">Contact</button>
          </nav>
        </div>
      </div>
    </header>


    <RouterView />
    <div
      class="flex-col justify-center md:text-5xl text-4xl space-y-5 p-5 md:mt-30 mt-12 md:mb-48 text-center text-white font-bold">
      <p>
      <p class="text-8xl font-extrabold p-2">#1</p>Construction Services</p>
      <p>Worldwide</p>
    </div>
    <div class="opacity-0 flex-col justify-center text-5xl md:mb-20 mb-52 text-center text-white font-bold">
      <button class="hover:bg-transparent"><img alt="logo" class="logo" src="" width="70" height="90" /></button>
    </div>

  </div>
  <div class="main">
    <About />
    <Features />
    <Liner />
    <Map />
    <Contact />
    <Information />
    <Footer />
  </div>
</template>

<style scoped>
.head {
  height: 80vh;
  background: linear-gradient(0deg, rgba(0, 0, 0, 3), rgba(0, 0, 0, 0.6)), url('https://wallpapers.com/images/hd/civil-engineering-construction-site-blueprint-0x148xb5hbkabmqu.jpg') no-repeat center;
  background-size: cover;

}

.main {
  height: 80vh;
}

.router-link-exact-active div {
  width: 50%;
  height: 0.25rem;
  margin-top: 0.25rem;
  margin-left: auto;
  margin-right: auto;
  border-radius: 9999px;
  /* background-color: #0d47a1; */
}

.notactive {
  text-align: center;
  z-index: 1;
  position: relative;
  overflow-y: hidden;
  width: 100%;
  height: 0vh;
  transition: ease-in 0.3s;
}

.active {
  height: 100%;
  width: 100%;
  background: #040404;
}

.bar1,
.bar2,
.bar3 {
  width: 35px;
  height: 3px;
  background-color: #0c0c0c;
  margin: 8px 5px;
  transition: 0s;
}
</style>
