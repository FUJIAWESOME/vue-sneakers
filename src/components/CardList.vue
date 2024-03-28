<script setup>
import Card from './Card.vue'

defineProps({
  items: Array
})
</script>

<template>
  <div class="grid grid-cols-4 gap-5 mt-10">
    <Card
      v-for="item in items"
      :key="item.id"
      :image-url="item.imageUrl"
      :title="item.title"
      :price="item.price"
      :is-added="true"
    />
  </div>
</template>
