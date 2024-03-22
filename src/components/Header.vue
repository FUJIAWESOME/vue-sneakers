<template>
  <header class="flex justify-between border-b border-slate-300 px-10 py-7">
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
        <b class="text-gray-500">1233 руб.</b>
      </li>
      <li class="flex items-center gap-2">
        <img src="/heart.svg" alt="heart" />
        <p class="text-gray-500">Закладки</p>
      </li>
      <li class="flex items-center gap-2">
        <img src="/profile.svg" alt="profile" />
        <p class="text-gray-500">Профиль</p>
      </li>
    </ul>
  </header>
</template>
