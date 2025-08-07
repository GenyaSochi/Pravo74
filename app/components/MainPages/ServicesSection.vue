<template>
  <div class="text-services container">
    <div v-for="el of heading" :key="el.id">
      <p class="heading-title">{{ el.title }}</p>
    </div>
    <div v-for="el of serv" :key="el.id">
      <p class="serv-title">{{ el.title }}</p>
      <p class="serv-text">{{ el.text1 }}</p>
    </div>
    <NuxtLink to="/services" class="serv-btn">подробнее</NuxtLink>
    <div v-for="el of family" :key="el.id">
      <p class="family-title">{{ el.title }}</p>
      <p class="family-text">{{ el.text1 }}</p>
      <NuxtLink to="/services" class="serv-btn">подробнее</NuxtLink>
    </div>
    <div v-for="el of orders" :key="el.id">
      <p class="orders-title">{{ el.title }}</p>
      <p class="orders-text">{{ el.text1 }}</p>
      <NuxtLink to="/services" class="serv-btn">подробнее</NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
import { NuxtLink } from '#components';

const heading = [
  { id: 1, title: 'Услуги' }
]

const serv = [
  { id: 1, title: 'Защита по делам об административных правонарушениях в области дорожного движения (ст. 12 КоАП РФ)' },
  { id: 2, title: 'ВЕРНУТЬ ПРАВА ОТ 10 000 ₽!', text1: 'Полный комплекс услуг дистанционно' }
]

const family = [
  { id: 1, title: 'Семейное право', text1: 'Комплексное юридическое сопровождение' }
]

const orders = [
  { id: 1, title: 'Судебные приказы', text1: 'Полный цикл юридического сопровождения' }
]
</script>

<style scoped>
.text-services {
  color: white;
  background-color: black;
  opacity: 0.9;
  padding: 20px;
  height: 460px;
}

.serv-btn {
  display: block;
  text-align: center;
  min-width: fit-content;
  color: white;
  background-color: #D4AF37;
  padding: 10px;
  border-radius: 5px;
  transition: background 0.5s ease, color 0.3s ease;
}

.serv-btn:hover {
  background: #0F1C3F;
  color: white;
  text-transform: uppercase;
}

.heading-title {
  text-transform: uppercase;
  font-size: 22px;
  padding-bottom: 20px;
  text-align: center;
}

.serv-title {
  text-transform: uppercase;
  font-size: 22px;
  text-align: center;
}

.serv-text {
  padding-bottom: 20px;
   text-align: center;
}

.family-title {
  text-transform: uppercase;
  font-size: 22px;
  padding-top: 20px;
  text-align: center;
}

.family-text {
  padding-bottom: 20px;
   text-align: center;
}

.orders-title {
  text-transform: uppercase;
  font-size: 22px;
  padding-top: 20px;
  text-align: center;
}

.orders-text {
  padding-bottom: 20px;
   text-align: center;
}
</style>