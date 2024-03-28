<script setup>
import { onMounted, ref, watch } from 'vue'
import axios from 'axios'

import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import Drawer from './components/Drawer.vue'

const items = ref([])
const filters = ref({
  sortBy: '',
  searchQuery: ''
})

const onChangeSort = (event) => {
  filters.value.sortBy = event.target.value
}

const onChangeSearch = (event) => {
  filters.value.searchQuery = event.target.value
}

const fetchItems = async () => {
  const params = {}

  if (filters.value.sortBy) {
    params.sortBy = filters.value.sortBy
  }

  if (filters.value.searchQuery) {
    params.title = `*${filters.value.searchQuery}*`
  }

  try {
    const { data } = await axios.get('https://d94d28be92d86424.mokky.dev/items', {
      params
    })
    console.log(data)
    items.value = data
  } catch (error) {
    console.log(error)
  }
}

onMounted(fetchItems)

watch(filters.value, fetchItems)
</script>

<template>
  <!-- <Drawer /> -->
  <div class="bg-white w-4/5 m-auto mt-10 rounded-xl shadow-xl">
    <Header />

    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold">Все кроссовки</h2>
        <div class="flex gap-10">
          <select
            @change="onChangeSort"
            class="text-gray-500 border rounded-xl outline-none py-3 px-3"
          >
            <option value="">Выберите сортировку</option>
            <option value="title">По названию</option>
            <option value="price">По цене (сначала дешевые)</option>
            <option value="-price">По цене (сначала дорогие)</option>
          </select>
          <div class="relative">
            <img class="absolute left-4 top-4" src="/search.svg" alt="search" />
            <input
              @input="onChangeSearch"
              class="text-gray-500 border rounded-xl outline-none py-3 pl-10 pr-3 focus:border-black"
              placeholder="Поиск..."
            />
          </div>
        </div>
      </div>
      <CardList :items="items" />
    </div>
  </div>
</template>
