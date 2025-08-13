<template>
  <div class="container main" v-for="el of help" :key="el.id">
    <h1>{{ el.heading }}</h1>
    <div>
      <p class="text">{{ el.info1 }}</p>
    </div>
    <h2 class="text">{{ el.info2 }}</h2>
  </div>

  <div>
    <div class="container card" v-for="el of text" :key="el.id">
      <p class="card_text">{{ el.cardText1 }}</p>    
        <p class="card_text">{{ el.cardText2 }}</p>
        <p class="card_text">{{ el.cardText3 }} {{ el.cardText4 }}</p>
    </div>
  
    <div class="container description" v-for="el of titledescr" :key="el.id">
      <h1>{{ el.titledescr1 }}</h1>
      <h2>{{ el.titledescr2 }}</h2>
      <h3>{{ el.titledescr3 }}</h3>
      <div v-for="el of descriptions" :key="el.id">
        <h4>{{ el.desc1 }}</h4>
        <ul>
          <li>{{ el.desc2 }}</li>
          <li>{{ el.desc3 }}</li>
        </ul>
      </div>
      <div v-for="el of protection" :key="el.id">
        <h4>{{ el.prot1 }}</h4>
        <ul>
          <li>{{ el.prot2 }}</li>
          <li>{{ el.prot3 }}</li>
          <li>{{ el.prot4 }}</li>
        </ul>
      </div>
      <div v-for="el of cases" :key="el.id">
        <h4>{{ el.cases1 }}</h4>
        <ul>
          <li>{{ el.cases2 }}</li>
          <li>{{ el.cases3 }}</li>
          <li>{{ el.cases4 }}</li>
        </ul>
      </div>
      <div v-for="el of final" :key="el.id">
        <h3>{{ el.final1 }}</h3>
        <ul>
          <li><strong>{{ el.final2 }}</strong></li>
          <li><strong>{{ el.final3 }}</strong>{{ el.final4 }}</li>
          <li><strong>{{ el.final5 }}</strong>{{ el.final6 }}</li>
          <li><strong>{{ el.final7 }}</strong>{{ el.final8 }}</li>
        </ul>
        <div>
          <p><strong>{{ el.final9 }}</strong></p>
          <p>{{ el.final10 }}</p>
          <button @click="popup = true" class="consult-btn">Записаться на консультацию</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const popup = ref(false)

const help = [
  { id: 1, heading: 'юридическая помощь по семейным и административным делам', info1: 'Отмена судебных приказов за 48 часов', info2: 'Юристы с 20-летним опытом в узкопрофильных направлениях права найдут оптимальное решение для вашего случая' }
]

const text = [
  { id: 1, cardText1: 'Благодаря многолетней практике и постоянному профессиональному развитию мы успешно завершаем более 400 дел в год', cardText2: 'Ежегодно мы предотвращаем сотни неправомерных списаний', cardText3: 'Мы работаем честно и открыто', cardText4: 'Предоставляем полное сопровождение — от консультации до судебных документов' }
]

const titledescr = [
  { id: 1, titledescr1: 'Юридическая помощь по семейным и административным делам', titledescr2: 'Профессиональное решение сложных правовых ситуаций', titledescr3: 'Мы предлагаем:' },
]

const descriptions = [
  { id: 1, desc1: 'Детальный анализ вашего случая', desc2: 'Оценка перспектив и возможных рисков', desc3: 'Прогноз развития ситуации' },
]

const protection = [
  { id: 1, prot1: 'Эффективную стратегию защиты', prot2: 'Досудебное урегулирование споров', prot3: 'Подготовка и подача исковых заявлений', prot4: 'Полное судебное сопровождение' }
]

const cases = [
  { id: 1, cases1: 'Комплексное ведение дела', cases2: 'Сбор и оформление документов', cases3: 'Представление интересов в судах и госорганах', cases4: 'Контроль исполнения решений', }
]

const final = [
  { id: 1, final1: 'Почему клиенты выбирают нас:', final2: 'Специалисты с практическим опытом от 10 лет', final3: 'Честная оценка шансов', final4: '— не обещаем невозможного', final5: 'Фиксированная стоимость услуг', final6: '— без скрытых платежей', final7: 'Конфиденциальность', final8: '— гарантия сохранения тайны', final9: 'Первая консультация — бесплатно!', final10: 'Получите ответы на ключевые вопросы и план действий уже сегодня' }
]
</script>
<!-- <template>
  <div class="container main">
    <div v-for="el of text" :key="el.id">
      <h1>{{ el.heading }}</h1>
      <p>{{ el.text1 }}</p>
      <p>{{ el.text2 }}</p>
      <p>{{ el.text3 }}</p>
      <p>{{ el.text4 }}</p>
      <p>{{ el.text5 }} {{ el.text6 }}</p>
      <p>{{ el.text7 }}</p>
      <p>{{ el.text8 }}</p>
      <p>{{ el.text9 }}</p>
      <p>{{ el.text10 }}</p>
    </div>
    <button @click="popup = true" class="consult-btn">Записаться на консультацию</button>
  </div>
</template>

<script setup lang="ts">
const popup = ref(false)

const text = [
  { id: 1, heading: 'Юридическая помощь по семейным и административным делам', text1: 'Отмена судебных приказов за 48 часов', text2: 'Юристы с 20-летним опытом в узкопрофильных направлениях права найдут оптимальное решение для вашего случая' },
  { id: 2, text1: 'Благодаря многолетней практике и постоянному профессиональному развитию мы успешно завершаем более 400 дел в год', text2: 'Ежегодно мы предотвращаем сотни неправомерных списаний', text3: 'Мы работаем честно и открыто', text4: 'Предоставляем полное сопровождение — от консультации до судебных документов' },
  { id: 3, text1: 'Юридическая помощь по семейным и административным делам', text2: 'Профессиональное решение сложных правовых ситуаций', text3: 'Мы предлагаем:' },
  { id: 4, text1: 'Детальный анализ вашего случая', text2: 'Оценка перспектив и возможных рисков', text3: 'Прогноз развития ситуации' },
  { id: 5, text1: 'Эффективную стратегию защиты', text2: 'Досудебное урегулирование споров', text3: 'Подготовка и подача исковых заявлений', text4: 'Полное судебное сопровождение' },
  { id: 6, text1: 'Комплексное ведение дела', text2: 'Сбор и оформление документов', text3: 'Представление интересов в судах и госорганах', text4: 'Контроль исполнения решений' },
  { id: 7, text1: 'Почему клиенты выбирают нас:', text2: 'Специалисты с практическим опытом от 10 лет', text3: 'Честная оценка шансов', text4: '— не обещаем невозможного', text5: 'Фиксированная стоимость услуг', text6: '— без скрытых платежей', text7: 'Конфиденциальность', text8: '— гарантия сохранения тайны', text9: 'Первая консультация — бесплатно!', text10: 'Получите ответы на ключевые вопросы и план действий уже сегодня' }
]
</script> -->

<style scoped>
.text {
  text-align: center;
  padding-top: 20px;
  font-size: 24px;
}

.main {
  background-color: black;
  color: white;
  opacity: 0.8;
  padding: 20px;
}

.card {
  display: flex;
  gap: 120px;
  padding: 20px;
  height: 400px;
  background-color: white;
  opacity: 0.8;
  margin: 0 auto;
  justify-content: center;
  align-items: center;
}

.card_text {
  background-color: black;
  width: 300px;
  height: 300px;
  border-radius: 20px;
  color: white;
  box-shadow: inset;
  padding: 20px;
  text-align: center;
}

.description {
  color: white;
  box-shadow: 0 0 25px rgba(255, 255, 255, 0.7);
  padding: 20px;
  text-align: center;
}

.consult-btn {
  background: #D4AF37;
  padding: 20px;
  border-radius: 10px;  
}

</style>
