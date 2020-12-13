<template>
  <div>
    <div class='flex justify-center'>
        <img style="height: 36rem" src="@/assets/image/FIRST_PAGE.png" usemap="#ImageMap" alt=""  >
    </div>
    <PageHeading>東京エリア/Tokyo</PageHeading>
    <ListTable class="my-4 lg:w-1/2 mx-auto" />
    <ListTableHtml class="my-4 lg:w-11/12 mx-auto" />
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'nuxt-composition-api'
import PageHeading from '@/components/page-heading.vue'
import ListTable from '@/components/list-table.vue'

export default defineComponent({
  components: {
    PageHeading,
    ListTable,
  },
})
</script>
<style></style>
