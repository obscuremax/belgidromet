<script setup>
import AppLayout from "./components/AppLayout.vue";
import AppCard from "./components/AppCard.vue";

const cards = [
  {
    title: 'Метеорология',
    image: 'meteorology.jpg'
  },
  {
    title: 'Радиолокация',
    image: 'meteoradar.jpg'
  },
  {
    title: 'Спутниковые снимки',
    image: 'sputnik.jpg'
  },
  {
    title: 'Гидрология',
    image: 'gidrology.jpg'
  },
  {
    title: 'Радиационный мониторинг',
    image: 'radiation.jpg'
  },
  {
    title: 'Рисамос',
    image: 'vibrosi.jpg'
  },
]

</script>

<template>
  <AppLayout :cardsCount="cards.length">
    <div class="card-list">
      <AppCard v-for="card in cards" :key="card.title" :card="card" />
    </div>
  </AppLayout>
</template>

<style lang="scss">
.card-list {
  --card-list-gap: 10px;
  padding: 20px 0;
  display: grid;
  grid-template-rows: auto;
  grid-template-columns: minmax(100px, 1fr);
  gap: var(--card-list-gap);
  height: inherit;
  @media (min-width: 480px) {
    --card-list-gap: 15px;
    grid-template-columns: repeat(2, minmax(100px, 1fr));
  }
  @media (min-width: 900px) {
    --card-list-gap: 20px;
  }
  @media (min-width: 1800px) {
    grid-template-columns: repeat(2, minmax(100px, 1fr));
  }
}
</style>