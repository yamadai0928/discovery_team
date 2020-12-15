<template>
  <div>
      <h1 class="text-4xl font-bold my-12 text-center">予約システム/Reservation</h1>
      <div class='flex justify-center'>
        <img style="height: 40rem" src="https://firebasestorage.googleapis.com/v0/b/discovery-307f1.appspot.com/o/calender.png?alt=media&token=8e48737c-972f-4d69-a5b0-67e5510c4499" usemap="#ImageMap" alt=""  >
      </div >
      <div class='flex justify-center'>
      <input type="date" class='' /> 
             <a role="button" class=" text-6x1 bg-red-600 hover:bg-red-700 text-white  px-4 py-2 mt-8 border rounded-full hover:underline" onclick= "location.href='/researvationOK'">
                    Reservation OK
                    </a>
      </div>
  </div>
</template>
<script lang="ts">

import { defineComponent, reactive, SetupContext } from 'nuxt-composition-api'
import PageHeading from '@/components/page-heading.vue'
import ListTable from '@/components/list2-table.vue'
import PlaceJson from '@/mock/place.json'
type PlaceList = {
  id: string,
  ku: string
}
