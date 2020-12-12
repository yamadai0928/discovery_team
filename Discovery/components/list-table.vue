<template>
  <div class="list-table shadow-md sm:rounded overflow-y-auto">
    <table class="w-full text-md bg-white">
      <thead>
        <tr class="border bg-teal-600 text-white">
          <th class="text-center p-4 px-10">23区エリア/Tokyo</th>
        </tr>
      </thead>
      <tbody class="text-gray-900">
        <tr
          v-for="(place, index) in PlaceList"
          :key="index"
          class="border-b bg-gray-100 hover:bg-orange-100 cursor-pointer"
          @click="PlaceLink(place.id)"
        >
          <td class="py-3 px-5 whitespace-no-wrap sm:whitespace-normal  text-center">
            {{ place.ku }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script lang="ts">
import { defineComponent, reactive } from 'nuxt-composition-api'
import PlaceJson from '@/mock/place.json'
type PlaceList = {
  id: string
  ku: string
}
export default defineComponent({
  name: 'ListTable',
  setup(_) {
    const PlaceList = reactive<PlaceList[]>(PlaceJson.PlaceData)
    const PlaceLink = (PlaceId: string): void => {
      // console.log("PlaceLink click")
      window.location.href = '/place/' + PlaceId
    }
    return {
      PlaceList,
      PlaceLink,
    }
  },
})
</script>
<style>
tbody tr:nth-child(odd) {
  @apply bg-white;
}
input[type='text'],
select {
  outline-color: #a0aec0;
}
</style>
