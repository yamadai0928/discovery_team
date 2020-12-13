<template>
  <div>
      <PageHeading>{{ placeData().ku }}</PageHeading>
      <div class='flex justify-center'>
        <img style="height: 36rem" src="@/assets/image/fig_kita_map_3.png" usemap="#ImageMap" alt=""  >
        <map name="ImageMap">
            <area shape="rect" coords="250,70,300,120" href="/company/0004" alt="" />
            <area shape="rect" coords="270,190,320,240" href="/company/0005" alt="" />
            <area shape="rect" coords="350,300,400,350" href="/company/0001" alt="" />
            <area shape="rect" coords="420,380,470,430" href="/company/0002" alt="" />
            <area shape="rect" coords="300,520,350,570" href="/company/0003" alt="" />
        </map>
      </div>
      <ListTable class="my-4 lg:w-1/2 mx-auto" />
      <ListTableHtml class="my-4 lg:w-3/4 mx-auto" />
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

export default defineComponent({
  setup(_, { root }: SetupContext) {
    const placeList = reactive<PlaceList[]>(PlaceJson.PlaceData)
    const placeData = (): PlaceList => {
      if (
        placeList.filter((place) => place.id === root.$route.params.id).length > 0
      ) {
        return placeList.filter((place) => place.id === root.$route.params.id)[0]
      }
      else {
        return {
          id: '',
          ku: '未指定'
        }
      }
    }

return {
      placeData
    }
  },

  components: {
    PageHeading,
    ListTable,
  },
})
</script>
<style></style>
