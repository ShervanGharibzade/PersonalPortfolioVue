<template>
  <div class="bg-zinc-900 overflow-hidden w-full overflow-y-scroll">
      <ReadMore @close="close" v-if="show" :pic="pic" />
    <div class="max-w-4xl mx-auto my-20 p-5 sm:p-20 md:p-20 lg:p-20 xl:p-20">
      <span class="bg-zinc-800 text-zinc-600 p-1">NEWS</span>
      <h2 class="flex-1 text-white my-4 text-3xl">Lastest News</h2>
      <div class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-2 mx-w-full gap-10">
        <div class="w-full">
          <div class="w-full lg:w-80 xl:w-80 group overflow-hidden">
            <img class="group-hover:scale-125 transition-all duration-300" src="../assets/images/1.9607929f.jpg"
                 alt="photo">
          </div>
          <div class="bg-black text-white p-5 w-full lg:w-80 xl:w-80 overflow-hidden relative">
            <span class="text-zinc-500 ">By Alex Watson05 April 2021</span>
            <p class="my-4 text-md sm:text-lg md:text-lg lg:text-lg xl:text-lg font-semibold">Format releases a new tool that enables direct video hosting</p>
            <button @click="Shoes"  class="group">
              <a class="absolute hover:tracking-widest text-sm transition-all duration-300 bottom-5">README
                MORE</a>
            </button>
          </div>
        </div>
        <div>
          <div class="w-full lg:w-80 xl:w-80 group overflow-hidden">
            <img class="group-hover:scale-125 transition-all duration-300" src="../assets/images/2.16917c10.jpg"
                 alt="photo">
          </div>
          <div class="bg-black text-white p-5 w-full lg:w-80 xl:w-80 overflow-hidden relative">
            <span class="text-zinc-500 ">By Alex Watson05 April 2021</span>
            <p class="my-4 text-md sm:text-lg md:text-lg lg:text-lg xl:text-lg font-semibold">Format releases a new tool that enables direct video hosting</p>
            <button @click="Shoes" class="group">
              <a class="absolute hover:tracking-widest text-sm transition-all duration-300  bottom-5">README
                MORE</a>
            </button>
          </div>
        </div>
        <div>
          <div class="w-full lg:w-80 xl:w-80 group overflow-hidden">
            <img class="group-hover:scale-125 transition-all duration-300" src="../assets/images/3.0cce3bce.jpg"
                 alt="photo">
          </div>
          <div class="bg-black text-white p-5 w-full lg:w-80 xl:w-80 overflow-hidden relative">
            <span class="text-zinc-500 ">By Alex Watson05 April 2021</span>
            <p class="my-4 text-md sm:text-lg md:text-lg lg:text-lg xl:text-lgfont-semibold">Format releases a new tool that enables direct video hosting</p>
            <button @click="Shoes" class="group">
              <a class="absolute transition-all duration-300 hover:tracking-widest text-sm bottom-5">README
                MORE</a>
            </button>
          </div>
        </div>
        <div>
          <div class="w-full lg:w-80 xl:w-80 group overflow-hidden">
            <img class="group-hover:scale-125 transition-all duration-300" src="../assets/images/4.58547fc5.jpg"
                 alt="photo">
          </div>
          <div class="bg-black text-white p-5 w-full lg:w-80 xl:w-80 overflow-hidden relative">
            <span class="text-zinc-500 ">By Alex Watson05 April 2021</span>
            <p class="my-4 text-md sm:text-lg md:text-lg lg:text-lg xl:text-lg font-semibold">Format releases a new tool that enables direct video hosting</p>
            <button @click="Shoes" class="group"> <a class="absolute hover:tracking-widest text-xs transition-all duration-300 bottom-5">README
                MORE</a>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex';
import ReadMore from "@/components/ReadMore";

export default {
  components: {ReadMore},
  data() {
    return {
        show:false
    }
  },
  computed: {
    ...mapState(["NewsPic"])
  },
  methods:{
    Shoes(){
      this.show = true;
    },
    close(){
      this.show = !this.show;
    }
  }
}
</script>
