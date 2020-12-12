<template>
  <div>
      <PageHeading>{{ placeData().ku }}</PageHeading>
      <div class='flex justify-center'>
        <img style="height: 36rem" src="@/assets/image/fig_kita_map_2.png" usemap="#ImageMap" alt=""  >
        <map name="ImageMap">
            <area shape="rect" coords="250,100,300,150" href="'/Company/0001'" alt="" />
            <area shape="rect" coords="250,225,300,275" href="'/Company/0002'" alt="" />
            <area shape="rect" coords="674,642,936,802" href="'/Company/0003'" alt="" />
            <area shape="rect" coords="793,785,1099,1005" href="'/Company/0004'" alt="" />
            <area shape="rect" coords="566,796,794,1050" href="'/Company/0005'" alt="" />
        </map>
      </div>
      <ListTable class="my-4 lg:w-11/12 mx-auto" />
      <ListTableHtml class="my-4 lg:w-11/12 mx-auto" />
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
