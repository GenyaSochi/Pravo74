<template>
  <header>
    <nav>
      <div class="all">
        <p class="text">Res iudicata pro veritate habetur</p>
        <button class="consult">заказать консультацию</button>
      </div>
      <div class="allheader">
        <NuxtLink to="/">главная</NuxtLink>
        <NuxtLink to="/services">услуги</NuxtLink>
        <NuxtLink to="/about">о нас</NuxtLink>
        <NuxtLink to="/reviews">отзывы</NuxtLink>
        <div class="info">
          <NuxtLink to="/contacts">+7-922-700-30-11</NuxtLink>
          <!-- <NuxtLink to="/contacts">pravo74.rf@yandex.ru</NuxtLink> -->
        </div>
      </div>

    </nav>
  </header>
</template>

<script setup lang="ts">
import { NuxtLink } from '#components';


</script>

<style scoped>
.all {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: black;
  color: white;
  font-size: 20px;
  padding: 10px;
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

.consult {
  background: #D4AF37;
  color: white;
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
  box-shadow: 0 0 10px rgba(212, 175, 55, 0.7);
}
</style>