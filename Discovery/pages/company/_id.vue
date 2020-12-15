<template>
  <div class="md h-screen">
      <div class="grid grid-cols-2">
          <div>
              <h1 class="text-6xl font-bold mt-0 text-left">{{company.name}}</h1>
              <!-- component -->
<!-- This is an example component -->
<div class="flex justify-center items-center">
  <div class="flex items-center mt-2 mb-4">
    <svg class="mx-1 w-4 h-4 fill-current text-yellow-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
    <svg class="mx-1 w-4 h-4 fill-current text-yellow-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
    <svg class="mx-1 w-4 h-4 fill-current text-yellow-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
    <svg class="mx-1 w-4 h-4 fill-current text-yellow-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
    <svg class="mx-1 w-4 h-4 fill-current text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
  </div>
</div>
<div class="grid grid-cols-3 gap-8">
          <div class=""> 
              <img :src="company.Picture.person_pic" 
                alt=""/>
          </div>
          <div class="col-span-2 mx-8"> 
              <h1 class="text-3x1 text-gray-900 font  ">{{company.information.infocomment}}</h1>
          <button class="text-5x1 mr-8 text-sm font-semibold hover:underline">
            read more
          </button>
          </div>
          </div>
              <p class="text-3x1 text-gray-900 font ">{{company.information.person}}</p>
              <div class="grid grid-cols-2 gap-8">
          <div class="flex mt-16 font-light text-gray-500 m-auto col-span-3"> 
            <div class="pr-4">
              <span class="uppercase">Since</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.information.since}}</p>
            </div>
            <div class="pr-4">
              <span class="uppercase">Adress</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.information.adress}}</p>
            </div>
            <div class="pr-4">
              <span class="uppercase">Category</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.information.category}}</p>
            </div>
          </div>
                       </div> 
       </div>  
          <div>
              <img :src="company.Picture.main_pic"
                class=" w-full" 
                alt=""/>
            </div>
      </div>
      <div class="grid grid-cols-2">
          <div>
              <h1 class="text-5xl font-sans mt-0 text-left">体験/Exercise</h1>
                 <div class="grid grid-cols-2 gap-8">
          <div class="flex mt-16 font-light text-gray-500 m-auto col-span-3">
            <div class="pr-4">
              <span class="uppercase">Opening time</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.Exercize.startingtime}}</p>
            </div>
            <div class="pr-4">
              <span class="uppercase">Exercize time</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.Exercize.exercizetime}}</p>
            </div>
            <div class="pr-4">
              <span class="uppercase">Price</span>
              <p class="text-lg text-gray-900 font-semibold pt-2">{{company.Exercize.price}}</p>
            </div>
            </div>
          </div>
            <div class="m-8">
                <p>{{company.Exercize.exercomment}}</p>
                </div> 
                <div class=" bg-red-600 hover:bg-red-700 text-white text-sm px-4 py-2 m-8 border rounded-full">
                    <a role="button" class='block no-underline text-center' onclick= "location.href='/researvation'">
                    Reservation
                    </a>
                 </div>
            <div>
                <p class="text-5xl font-sans mt-4 text-left">地図/Map</p>
            <img :src="company.Picture.map_pic"
                class="my-10 w-11/12"
                alt=""/>
            </div>
          </div>
          <div>
              <img :src="company.Picture.exercize_pic"
                class=" w-full"
                alt=""/>
                  <h1 class="text-3xl font-sans mt-4 text-left">レビュー/Review</h1>
<div class="flex items-start">
  <div class="flex-shrink-0">
    <div class="inline-block relative">
      <div class="relative w-16 h-16 rounded-full overflow-hidden">
        <img class="absolute top-0 left-0 w-full h-full bg-cover object-fit object-cover" src="https://firebasestorage.googleapis.com/v0/b/discovery-307f1.appspot.com/o/aaaa.png?alt=media&token=4b908a4f-83b8-4b7c-9ae3-4fa1583d11b5" alt="Profile picture">
        <div class="absolute top-0 left-0 w-full h-full rounded-full shadow-inner"></div>
      </div>
      <svg class="fill-current text-white bg-green-600 rounded-full p-1 absolute bottom-0 right-0 w-6 h-6 -mx-1 -my-1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
        <path d="M19 11a7.5 7.5 0 0 1-3.5 5.94L10 20l-5.5-3.06A7.5 7.5 0 0 1 1 11V3c3.38 0 6.5-1.12 9-3 2.5 1.89 5.62 3 9 3v8zm-9 1.08l2.92 2.04-1.03-3.41 2.84-2.15-3.56-.08L10 5.12 8.83 8.48l-3.56.08L8.1 10.7l-1.03 3.4L10 12.09z"/>
      </svg>
    </div>
  </div>
  <div class="ml-6">
      <h1 class="text-5xl font-sans mt-4 text-left"></h1>
    <p class="flex items-baseline">
      <span class="text-gray-600 font-bold">山下/Yamashita</span>
      <span class="ml-2 text-green-600 text-xs">yamashita@gmail.com</span>
    </p>
    <div class="flex items-center mt-1">
      <svg class="w-4 h-4 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
      <svg class="w-4 h-4 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
      <svg class="w-4 h-4 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
      <svg class="w-4 h-4 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
      <svg class="w-4 h-4 fill-current text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
    </div>
    <div class="flex items-center mt-4 text-gray-600">
      <div class="flex items-center">
        <span class="text-sm">サービス</span>
        <div class="flex items-center ml-2">
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
        </div>
      </div>
      <div class="flex items-center ml-4">
        <span class="text-sm">体験</span>
        <div class="flex items-center ml-2">
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-yellow-600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
          <svg class="w-3 h-3 fill-current text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M10 15l-5.878 3.09 1.123-6.545L.489 6.91l6.572-.955L10 0l2.939 5.955 6.572.955-4.756 4.635 1.123 6.545z"/></svg>
        </div>
      </div>
    </div>
    <div class="mt-3">
      <span class="font-bold">{{company.Review.comment}}</span>
      <p class="mt-1"></p>
    </div>
    <div class="flex items-center justify-between mt-4 text-sm text-gray-600 fill-current">
      <div class="flex items-center">
        <span></span>

      </div>
    </div>
  </div>
</div>
            </div>
      </div>
  </div>
</template>

<script lang="ts">

import { defineComponent, reactive, SetupContext } from 'nuxt-composition-api'
import PageHeading from '@/components/page-heading.vue'
import companyJson from '@/mock/companylist.json'
type Company = {
  id: string,
  name: string,
  information: {
    person: string,
    adress: string,
    category: string,
    since: string,
    infocomment: string,
  }
  Excersize: {
    startingtime: string,
    exercizetime: string,
    price: string,
    exercomment: string,
  }
  Picture:{
    main_pic : string,
    person_pic : string,
    map_pic : string,
    exercixe_pic: string,
  }
  Review:{
    comment : string,
  } 
}
export default defineComponent({
  setup(_, { root }: SetupContext) {
    const companyList = reactive<Company[]>(companyJson.companyData)
    const filteredCompanyList = companyList.filter((c) => c.id === root.$route.params.id)
    const company = filteredCompanyList[0]
    return {
      company,
    }
  }
})
</script>
<style></style>

