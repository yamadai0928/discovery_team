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
              <h1 class="text-5xl font-sans mt-0 text-left">Exercise</h1>
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
            <div class="mx-1">
                <p>{{company.Exercize.exercomment}}</p>
                </div> 
            <div>
                <p class="text-5xl font-sans mt-4 text-left">Map</p>
            <img :src="company.Picture.map_pic"
                class="my-10 w-11/12"
                alt=""/>
            </div>
          </div>
          <div>
              <img :src="company.Picture.exercize_pic"
                class=" w-full"
                alt=""/>
                <button class="text-4x1 uppercase m-8 font-semibold hover:underline">
            Reservation
          </button>
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

