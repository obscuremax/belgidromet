<script setup>
import {computed} from "vue";

const props = defineProps({
  card: {
    type: Object,
    default: () => ({
      title: 'Метеорология',
      image: 'meteorology.jpg'
    }),
  },
})
const {title, image} = props.card;
const bgImage = computed(() => `background-image: url("./${image}")`);
</script>

<template>
    <a class="card" href="#">
      <div class="card__front" :style="bgImage">
        <div class="card__title">{{title}}</div>
        <div class="card__back">
          <button class="card__button" type="button">Перейти</button>
        </div>
      </div>
    </a>
</template>

<style scoped lang="scss">
$transition-time: 2.3s;
.card {
  position: relative;
  height: 100%;
  width: 100%;
  display: flex;
  transition: ease all $transition-time;
  perspective: 1200px;
  &__title {
    font-weight: 600;
    position: absolute;
    bottom: 20px;
    left: 0;
    padding: 0 20px;
    color: white;
    text-shadow: 2px 2px 5px var(--darkenTheme);
    transform-style: preserve-3d;
    transition: ease all $transition-time;
    z-index: 3;
    font-size: 25px;
    transform: translateZ(0px);
  }
  &__button {
    cursor: pointer;
    transform-style: preserve-3d;
    transition: ease transform $transition-time, ease background .5s;
    transform: translateZ(-1px) rotatey(-180deg);
    border: none;
    border-radius: 5px;
    font-weight: 600;
    font-size: 15px;
    color: var(--darkenTheme);;
    padding: 10px 20px;
    outline: none;
    text-decoration: none;
    background-color: var(--primaryTheme);
    @media (hover: hover) {
      &:hover {
        background-color: var(--lightTheme);
      }
    }
  }
  &__front {
    position: absolute;
    height: 100%;
    width: 100%;
    transform-style: preserve-3d;
    transition: ease all $transition-time;
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    border-radius: 10px;
    border: 1px solid var(--primaryTheme);
  }
  &__back {

    position: absolute;
    height: 100%;
    width: 100%;
    background: var(--darkTheme);
    transform-style: preserve-3d;
    transition: ease all $transition-time;
    transform: translateZ(-1px);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 10px;
    border: 1px solid var(--primaryTheme);
  }
  @media (hover: hover) {
    &:hover {
      .card__front {
        transform: rotateX(0deg) rotateY(-180deg);
        .card__title {
          transform: translateZ(100px);
        }
        .card__button {
          transform: translateZ(-60px) rotatey(-180deg);
        }
      }
    }
  }
}
</style>