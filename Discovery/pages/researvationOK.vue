<template>
  <div>
      <h1 class="text-4xl font-bold my-12 text-center">予約完了</h1>
      <div class='flex justify-center'>
      </div >
      <div class='flex justify-center'>
             <a role="button" class=" text-6x1 bg-red-600 hover:bg-red-700 text-white  px-4 py-2 mt-8 border rounded-full hover:underline" onclick= "location.href='/list'">
                    戻る
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
