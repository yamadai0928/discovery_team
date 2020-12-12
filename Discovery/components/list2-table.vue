<template>
  <div class="list-table shadow-md sm:rounded overflow-y-auto">
    <table class="w-full text-md bg-white">
      <thead>
        <tr class="border bg-teal-600 text-white">
          <th class="text-center p-4 px-10">店名/shopname</th>
        </tr>
      </thead>
      <tbody class="text-gray-900">
        <tr
          v-for="(company, index) in CompanyList"
          :key="index"
          class="border-b bg-gray-100 hover:bg-orange-100 cursor-pointer"
          @click="CompanyLink(company.id)"
        >
          <td class="py-3 px-5 whitespace-no-wrap sm:whitespace-normal  text-center">
            {{ company.name }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
<script lang="ts">
import { defineComponent, reactive } from 'nuxt-composition-api'
import CompanylistJson from '@/mock/companylist.json'
type CompanyList = {
  id: string
  name: string
}
export default defineComponent({
  name: 'ListTable',
  setup(_) {
    const CompanyList = reactive<CompanyList[]>(CompanylistJson.CompanyData)
    const CompanyLink = (CompanyId: string): void => {
      window.location.href = '/Company/' + CompanyId
    }
    return {
      CompanyList,
      CompanyLink,
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
