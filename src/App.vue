<script setup>
const cards = [
  {
    title: 'Метеорология',
    image: 'meteorology.jpg'
  },{
    title: 'Радиолокация',
    image: 'meteoradar.jpg'
  },{
    title: 'Спутниковые снимки',
    image: 'sputnik.jpg'
  },{
    title: 'Гидрология',
    image: 'gidrology.jpg'
  },{
    title: 'Радиационный мониторинг',
    image: 'radiation.jpg'
  },{
    title: 'Рисамос',
    image: 'vibrosi.jpg'
  },
]
const bgImage = (image) => `background-image: url("./${image}")`
</script>

<template>
  <div>
    <section class="container-cards">

          <div class="card" v-for="card in cards">
            <div class="cover" :style="bgImage(card.image)">
              <h1>{{card.title}}</h1>
<!--              <span class="price">$35</span>-->
              <div class="card-back">
                <a href="#">Перейти</a>
              </div>
            </div>
          </div>

    </section>
  </div>
</template>