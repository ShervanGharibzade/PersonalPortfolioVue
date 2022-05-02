<template>
  <div class="bg-zinc-900 w-full overflow-hidden overflow-y-scroll">
    <div v-for="user in members" class=" p-10">
      <div v-if="user.fullName === 'Adriano & Smith'" class="max-w-4xl my-20 mx-auto">
        <img class="w-full mx-auto mt-32" :src='user.url' alt="photo">
        <div class="grid w-full sm:flex md:text-start lg:text-start xl:text-start md:flex lg:flex xl:flex text-xm">
          <div class="w-2/3 md:w-2/3 lg:w-2/3 xl:w-2/3">
            <h3 class="lg:text-3xl xl:text-3xl text-2xl text-white mt-10">{{ user.fullName }}</h3>
            <p class="text-zinc-400 xl:text-xl lg:text-xl  my-2">{{user.message}}</p>
            <button class="bg-zinc-200 transition-all duration-300 hover:tracking-widest p-3 my-3 hover:pr-5 hover:">Read more</button>
          </div>
          <div class="w-full sm:w-1/3 md:w-1/3 lg:w-1/3 mt-10">
            <ul class="text-xs w-full md:text-xl lg:text-xl xl:text-xl">
              <li class="flex w-full text-white">Birthday:
                <span class="ml-6 w-full">{{user.Birthday}}</span>
              </li>
              <li class="flex text-white">Age:
                <span class="ml-14">{{user.Age}}</span>
              </li>
              <li class="flex w-50 text-white">Address:
                <div class="ml-6 w-full w-50">{{user.Address}}</div>
              </li>
              <li class="flex text-white">Email:
                <span class="ml-11">{{user.Email}}</span>
              </li>
              <li class="flex text-white">Phone:
                <span class="ml-9">{{user.Phone}}</span>
              </li>
              <li class="flex text-white">Study:
                <span class="ml-11">{{user.Study}}</span>
              </li>
              <li class="flex text-white">Freelance:
                <span class="ml-5">{{user.Freelance}}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {mapState} from 'vuex'

export default {
  computed:{
    ...mapState([
      'members'
    ])
  }
}
</script>
