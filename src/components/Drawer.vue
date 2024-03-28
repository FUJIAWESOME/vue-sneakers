<script setup>
import CartList from './CartList.vue'
import CartHeader from './CartHeader.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full bg-black/70 z-20">
    <div class="fixed top-0 right-0 w-96 h-full bg-white p-8">
      <CartHeader />
      <CartList />

      <div class="flex flex-col justify-between">
        <div class="flex flex-col gap-4 mt-10">
          <div class="flex justify-between gap-2">
            <p>Итого:</p>
            <div class="flex-1 border-b border-dashed"></div>
            <b>1233 руб.</b>
          </div>
          <div class="flex justify-between gap-2">
            <p>Налог 5%:</p>
            <div class="flex-1 border-b border-dashed"></div>
            <b>1233 руб.</b>
          </div>
        </div>
        <button
          :disabled="false"
          class="cursor-pointer rounded-3xl p-3 mt-3 w-full bg-lime-500 text-white hover:bg-lime-600 active:bg-lime-700 disabled:bg-gray-500"
        >
          Оформить
        </button>
      </div>
    </div>
  </div>
</template>
