<template>
  <header>
    <nav class="allheader">
      <NuxtLink to="/">главная</NuxtLink>
      <NuxtLink to="/services">услуги</NuxtLink>
      <NuxtLink to="/about">о нас</NuxtLink>
      <NuxtLink to="/reviews">отзывы</NuxtLink>
      <button>консультация</button>
      <NuxtLink to="/contacts">pravo74.rf@yandex.ru</NuxtLink>
      <NuxtLink to="/contacts">+7-922-700-30-11</NuxtLink>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { NuxtLink } from '#components';


</script>

<style scoped>
.allheader {
  display: flex;
  justify-content: space-around;
  gap: 20px;
  padding: 20px 0;
  
}
</style>