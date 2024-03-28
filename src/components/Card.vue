<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number,
  isAdded: Boolean,
  isFavorite: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>

<template>
  <div
    class="relative p-8 border rounded-3xl cursor-pointer transition hover:-translate-y-2 hover:shadow-2xl"
  >
    <img
      :src="isFavorite ? '/like-2.svg' : '/like-1.svg'"
      alt="like"
      class="absolute transition hover:-translate-y-1 hover:shadow-2xl hover:scale-110"
    />
    <img :src="imageUrl" alt="sneaker" />

    <p class="mt-5">{{ title }}</p>

    <div class="flex justify-between mt-5">
      <div class="flex flex-col">
        <span class="text-gray-300 uppercase">Цена:</span>
        <b>{{ price }} руб.</b>
      </div>

      <img
        :src="isAdded ? '/checked.svg' : '/plus.svg'"
        alt="plus"
        class="transition hover:-translate-y-1 hover:shadow-2xl hover:scale-110"
      />
    </div>
  </div>
</template>
