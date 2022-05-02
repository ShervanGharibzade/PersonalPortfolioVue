<template>
  <div class="bg-black z-20 xl:z-0 w-full h-16 fixed xl:relative text-white xl:h-full xl:w-96 text-start">
    <div class="relative flex xl:grid ml-10 top-0 2xl:top-44 sm:ml-20 md:ml-20 lg:ml-20 xl:ml-20">
      <h2 class="text-2xl flex-1 my-0 sm:flex-1 md:flex-1 lg:flex-1 lx:flex-1 xl:my-8 mt-2 font-mono font-black tracking-widest">TOKTO</h2>
      <ul class="text-gray-400 flex sm:mr-16 md:mr-16 lg:mr-16 xl:mr-16 bg-black rounded sm:border-0 md:border-0 lg:border-0 xl:border-0 relative sm:top-0 md:top-0 lg:top-0 xl:top-0 sm:flex md:flex lg:flex xl:flex xl:grid">
        <li @click="DisplayHome" class="cursor-pointer my-2 transition-all focus:text-blue-500 hover:text-white duration-300 hover:tracking-widest">
          <span  class="hidden xl:block">Home</span>
          <span>
            <i class="fa fa-home block xl:hidden px-2 mt-3" aria-hidden="true"></i>
          </span>
        </li>
        <li @click="DisplayAbout" class="cursor-pointer my-2 transition-all hover:text-white duration-300 hover:tracking-widest">
          <span class="hidden xl:block">About</span>
          <span>
            <i class="fa fa-user block xl:hidden px-2 mt-3" aria-hidden="true"></i>
          </span>
        </li>
        <li @click="DisplayPortfolio" class="cursor-pointer my-2 transition-all hover:text-white duration-300 hover:tracking-widest">
          <span class="hidden xl:block">Portfolio</span>
          <span>
            <i class="fa fa-inbox block xl:hidden px-2 mt-3" aria-hidden="true"></i>
          </span>
        </li>
        <li @click="DisplayNews" class="cursor-pointer my-2 transition-all hover:text-white duration-300 hover:tracking-widest">
          <span class="hidden xl:block">News</span>
          <span>
            <i class="fa fa-file-text-o block xl:hidden px-2 mt-3"  aria-hidden="true"></i>
          </span>
        </li>
        <li @click="DisplayContact" class="cursor-pointer my-2 transition-all hover:text-white duration-300 hover:tracking-widest">
          <span class="hidden xl:block">Contact</span>
          <span>
            <i class="fa fa-envelope-o block xl:hidden px-2 mt-3" aria-hidden="true"></i>
          </span>
        </li>
      </ul>
      <p class="text-gray-400 italic hidden xl:block mt-8">© 2022 Tokyo VueJS
        <br>
        Created by
        <span class="transition-all duration-300 hover:text-white hover:tracking-widest">Ib-Themes</span>
      </p>
    </div>
  </div>
</template>

<script>
import {mapActions} from 'vuex';

export default {
  data() {
    return {}
  },
  methods:{
    DisplayHome() {
      this.$emit('Home')
    },
    DisplayAbout() {
      this.$emit('About')
    },
    DisplayPortfolio() {
      this.$emit('Portfolio')
    },
    DisplayNews() {
      this.$emit('News')
    },
    DisplayContact() {
      this.$emit('contact')
    }
  }
}
</script>
