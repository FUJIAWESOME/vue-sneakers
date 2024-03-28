<script setup>
defineProps({
  imageUrl: String,
  title: String,
  price: Number
  // isAdded: Boolean,
  // isFavorite: Boolean,
  // onClickAdd: Function,
  // onClickFavorite: Function
})
</script>

<template>
  <div class="flex justify-between border rounded-xl p-4">
    <div class="flex items-center">
      <img class="w-20" src="/sneakers/sneakers-1.jpg" alt="sneaker" />
      <div class="ml-4">
        <p>Кроссовки Vans</p>
        <b>1233 руб.</b>
      </div>
    </div>
    <img class="cursor-pointer transition hover:-translate-y-1" src="/close.svg" alt="close" />
  </div>
</template>
