<template>
  <header class="flex justify-between border-b border-gray-300 px-10 py-7">
    <div class="flex items-center gap-3">
      <img class="w-10" src="/logo.png" alt="logo" />
      <div>
        <p class="text-xl font-bold uppercase">Vue Sneakers</p>
        <p class="font-normal text-gray-400">Магазин лучших кроссовок</p>
      </div>
    </div>

    <ul class="flex gap-6">
      <li class="flex items-center gap-2">
        <img src="/cart.svg" alt="cart" />
        <p class="text-gray-500 hover:text-black cursor-pointer">1233 руб.</p>
      </li>
      <li class="flex items-center gap-2">
        <img src="/heart.svg" alt="heart" />
        <p class="text-gray-500 hover:text-black cursor-pointer">Закладки</p>
      </li>
      <li class="flex items-center gap-2">
        <img src="/profile.svg" alt="profile" />
        <p class="text-gray-500 hover:text-black cursor-pointer">Профиль</p>
      </li>
    </ul>
  </header>
</template>
