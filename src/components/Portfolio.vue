<template>
  <div class="bg-zinc-900 overflow-hidden w-full overflow-y-scroll" >
    <div class="max-w-4xl mx-auto my-20 p-5 md:p-20 lg:p-20 xl:p-20">
      <span class="bg-zinc-800 text-zinc-600 p-1">PORTFOLIO</span>
      <div class="grid sm:flex md:flex lg:flex xl:flex text-white mt-3">
        <h2 class="flex-1 text-xl sm:text-3xl md:text-3xllg:text-3xl xl:text-3xl">Creative Portfolio</h2>
        <ul class="flex flex-1 text-xs sm:text-2xl md:text-2xl lg:text-2xl xl:text-2xl">
          <li @click="All" class="pr-2 cursor-pointer mt-2 transition-all duration-300 hover:tracking-widest">All</li>
          <li @click="Vimeo" class="px-2 cursor-pointer mt-2 transition-all duration-300 hover:tracking-widest">Vimeo</li>
          <li @click="youtube" class="px-2 cursor-pointer mt-2 transition-all duration-300 hover:tracking-widest">Youtube</li>
          <li @click="mix" class="px-2 cursor-pointer mt-2 transition-all duration-300 hover:tracking-widest">Mix</li>
          <li @click="All" class="px-2 cursor-pointer mt-2 transition-all duration-300 hover:tracking-widest">Gallery</li>
        </ul>
      </div>
      <div class="grid justify-center grid-cols-1 xl:w-full lg:w-full lg:grid-cols-2 xl:grid-cols-2 mx-auto gap-10 w-ful md:w-96 relative mt-0 md:mt-20 lg:mt-20 xl:mt-20">
        <div  v-for="user in members">
          <div class="h-full overflow-hidden  w-full h-96 group">
            <img v-show="allPic" v-if="user.Gender === 'female' " class="transition-all w-full duration-300 group-hover:scale-125" :src="user.url" alt="photo">
            <img v-show="vimeoPic" v-if="user.job === 'Developer' " class="transition-all duration-300 group-hover:scale-125" :src="user.url" alt="photo">
            <img v-show="youtubePic" v-if="user.job === 'Designer' " class="transition-all duration-300 group-hover:scale-125" :src="user.url" alt="photo">
            <img v-show="mixPic" v-if="user.job === 'Designer'" class="transition-all duration-300 group-hover:scale-125" :src="user.url" alt="photo">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex';

export default {
  computed: {
    ...mapState(["members"]),

  },
  data(){
    return{
      allPic:true,
      vimeoPic:false,
      youtubePic:false,
      mixPic:false,
      galleryPic:false
    }
  },
  methods:{
    All(){
      this.allPic = true;
      this.mixPic = false;
      this.vimeoPic = false;
      this.youtubePic = false;
    },
    Vimeo(){
      this.allPic = false;
      this.mixPic = false;
      this.vimeoPic = true;
      this.youtubePic = false;
    },
    youtube(){
      this.allPic = false;
      this.mixPic = false;
      this.vimeoPic = false;
      this.youtubePic = true;
    },
    mix(){
      this.allPic = false;
      this.mixPic = true;
      this.vimeoPic = false;
      this.youtubePic = true;
    }
  }
}
</script>
