<template>
  <header>
    <nav class="all">
      <div class="allheader">
        <NuxtLink to="/">главная</NuxtLink>
        <NuxtLink to="/services">услуги</NuxtLink>
        <NuxtLink to="/about">о нас</NuxtLink>
        <NuxtLink to="/reviews">отзывы</NuxtLink>
        <div class="info">
          <NuxtLink to="/contacts">+7-922-700-30-11</NuxtLink>
          <NuxtLink to="/contacts">pravo74.rf@yandex.ru</NuxtLink>
        </div>
      </div>
      <p class="text">Res iudicata pro veritate habetur</p>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { NuxtLink } from '#components';


</script>

<style scoped>
.all {
  background-color: black;
  color: white;
  font-size: 20px;
}

.allheader {
  display: flex;
  font-size: 16px;
  gap: 20px;
  align-items: center;
  justify-content: space-evenly;
  padding: 10px;
}

.info {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.text {
  text-align: start;
  font-size: 16px;
  padding-left: 10px; 
}
</style>