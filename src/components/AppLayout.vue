<script setup>
import {computed} from "vue";
const props = defineProps({
  cardsCount: {
    type: Number,
    default: 1
  }
})
const {cardsCount} = props
const maxHeight = computed(() => {
  if (cardsCount < 3) return 'max-height: 33%';
  if (cardsCount < 5)return 'max-height: 66%';
  return 'max-height: 100%';
})
</script>

<template>
  <div class="page-layout">
    <header class="header">
      <div class="header__container container">
        <a class="logo-link" href="https://www.belgidromet.by/" target="_blank">
          <svg xmlns="http://www.w3.org/2000/svg" version="1.0" width="50" height="50" viewBox="0 0 256 213">
            <path d="M121.6 3.7c-2.1 2.1-4.7 5.7-5.8 8.1l-2 4.3-6.7-.3c-6.6-.3-6.7-.2-11.9 4.2-2.9 2.5-5.5 5.5-5.9 6.8-.9 3.9.3 11.2 2.2 12.6 1.4 1 1.5 1.7.6 3.4-1.1 2.2-2.2 2.6-8.3 3.6-3.2.6-3.7 1-4 3.9-.3 2.8-.7 3.2-4.4 4-2.9.5-4.3 1.4-4.7 2.7-.5 1.9-1.5 2-17.1 2H37v3.1c0 6.6.7 6.9 15.2 6.9h13l-.7 2.2c-.3 1.3-.9 3.3-1.2 4.5-.4 1.9-1.2 2.3-4.4 2.3-2.2 0-3.9-.5-3.9-1 0-.6-.7-1-1.5-1s-1.5.4-1.5 1-3.7 1-9 1-9-.4-9-1-.7-1-1.5-1c-1.2 0-1.5 1.5-1.5 7.5V91h7.1c5.2 0 7 .3 6.7 1.2-.3.9-3 1.4-7.6 1.6-6.9.3-7.2.4-7.2 2.7 0 2.5-.1 2.5-8.9 2.5-5 0-9.2.4-9.5.9-.7 1.1 1.8 18.3 3.5 24.3.7 2.4 1.8 5 2.6 5.9.8.9 1.3 4.1 1.3 8 0 3.5.5 8.2 1.1 10.4 1 3.7.9 4.1-1.6 6.2-1.4 1.3-3.7 2.3-4.9 2.3-3 0-6.9 3.1-10.7 8.6-4.4 6.5-3.8 9 3.4 13.8l5.9 3.9-.8 4.6c-.5 2.5-.8 6.8-.9 9.6v5l6.9.9c6.6.8 7.1.7 8.4-1.3.8-1.1 2-2.1 2.7-2.1 1.6 0 4.5-3.3 4.5-5.2 0-.9.6-2 1.3-2.7 1.8-1.4 34.9-2.2 40.7-.9 2.5.5 6.2 1.2 8.2 1.5 2.1.3 4.2 1.1 4.9 1.9.6.8 2.2 1.4 3.5 1.4 1.2 0 3.5.5 5.1 1.1 1.5.6 4.7 1.1 7.1 1 3-.1 4.2.2 4.2 1.2 0 2.7 3.5 4.7 8.4 4.7 4.1 0 4.8.3 5.6 2.6 1.3 3.3 5.3 3 5.8-.4.3-1.8.8-2.1 2.7-1.6 1.3.3 3.3.1 4.4-.6 1.7-.8 2.6-.8 4.3.5 1.5 1 3.3 1.3 5.5.9 3-.6 3.4-.4 4.4 2.5 1.4 3.9 3.4 4 5.4.1 1.3-2.5 7.9-6.9 8.9-5.9.2.2 1.1 2.6 1.9 5.4 1.3 4.5 1.7 5 4.2 4.8 1.6-.1 4-1.4 5.5-2.8 3.1-3 3.7-3 6.3-.8 1.8 1.7 2 1.7 3.7-.5 2.3-2.7 7.2-3.9 8.7-2 .6.7 1.3 2.2 1.5 3.3.4 2.4 2.5 2.9 6.1 1.6 2.2-.9 2.7-1.7 2.6-4.3 0-1.8-.4-4.2-.8-5.3-.6-1.3-.3-2.8.9-4.5.9-1.4 2.3-4.3 3-6.5.7-2.2 2.1-5.4 3.1-7.1 1.1-1.7 1.9-3.9 1.9-4.8 0-1.2 1-1.6 4.4-1.6 2.7 0 4.8-.6 5.6-1.5.9-1.1 2.2-1.4 4.1-1 6 1.3 9.5-4.8 4.9-8.8-1.6-1.3-2-2.9-2-7.4-.1-3.5-.6-6.6-1.5-7.7-.8-1.1-1.5-3.4-1.5-5.1 0-2-.8-3.9-2.1-5.1-1.2-1-3-3.2-4.1-4.7-2-2.8-2-2.9-.2-6.2 1.6-3 2.1-3.3 4.8-2.8 1.7.3 3.8 1.2 4.6 1.9 4.9 4.2 13.4 2.3 18.7-4.3 2.1-2.5 4.8-5.6 6.1-6.9 3.4-3.5 2.9-6.6-1.5-9.5-2.1-1.3-4.5-3.8-5.3-5.6-1.6-3.5-7.6-6.3-13.5-6.3-2.8 0-3.2-.3-2.8-2.3.3-1.3-.2-4-1-5.9-1.2-2.8-2.3-3.8-4.9-4.3-6.9-1.6-9.9-3.8-12.8-9.6-2.2-4.3-2.7-6.4-2.3-9.5l.5-3.9-5.6-2.4c-6.2-2.5-6.7-3.7-3.9-9.5 1.4-3.1 1.5-4.2.4-8.3-.7-2.7-1.4-8.4-1.4-12.8-.2-7.7-.3-8-2.7-8.3-1.4-.2-4.1-1.8-6-3.7-7-6.6-17.3-7.2-25.5-1.5-4.8 3.3-5.9 2.9-5.4-2.1.4-4.6-.1-5.7-3.2-6.8-4.5-1.5-9.4-1.4-10.9.4-1.7 2.1-2.3 1.9-4.3-1.5-1.9-3.2-5.1-3.9-8.7-2-1.3.7-2.1.6-3-.5-2-2.4-4.4-1.8-8.4 2.2zm7.5 1.9c1.6 1.4 2.3 1.5 4.9.4 3.3-1.4 5.4-.4 6.5 3.1.8 2.3 4.7 2.5 6.5.4.9-1.1 2.7-1.5 5.4-1.3l4.1.3.3 5.1c.2 4.2.7 5.3 2.6 6.4 2.1 1.1 2.9.9 7.1-2 9.1-6.3 16.9-5.7 23.9 1.9 1.7 1.7 3.6 3.1 4.4 3.1 1.2 0 1.4 1.1.9 5.5-.4 3.9 0 6.7 1.3 10.3 1.8 4.7 1.8 4.9-.1 9.1-3.4 7.7-2.2 10.5 5.4 13.2 3.5 1.2 3.8 1.6 3.3 4.2-.4 2 .4 4.8 2.9 9.8 3.1 6.1 4.1 7.2 8.3 9 8.9 4 9.7 4.5 10 6.3.2 1-.2 2.2-.9 2.6-1 .7-1 1.5.1 4 1.3 3 1.6 3.2 5.3 2.7 5.7-.8 11 1.6 13 5.8.9 1.9 3 4.1 4.7 5 1.6.8 3 1.8 3 2.1 0 1.2-8.5 11.1-10.9 12.6-3.4 2.3-7.2 2.3-10.4-.2-1.7-1.3-4-2-7.1-2-4.3 0-4.6.2-7.1 4.3-1.4 2.4-2.5 5.1-2.5 5.9 0 .9 2.1 3.9 4.6 6.7 3.6 4 4.5 5.7 4 7.5-.3 1.3.1 3.1.9 4.2.8 1 1.5 3.7 1.5 5.9 0 5 1.8 11.5 3 11.5.6 0 1 .4 1 1 0 .5-2 1-4.5 1s-4.5.4-4.5 1c0 .5-1.8 1-4.1 1-5.2 0-7.9 1.5-7.9 4.3 0 1.2-.9 3.5-2 5.2-1.1 1.6-2 3.9-2 5 0 1.8-1.5 4.6-5.2 9.7-1 1.4-.9 2.4.5 5.3 2.2 4.6 1.1 6.7-1.3 2.7-1-1.7-2.8-3.3-3.9-3.7-2.1-.6-8.8 1-10.5 2.6-.5.4-2 .1-3.3-.8-2.3-1.5-2.5-1.5-5.6 1.6-4 3.8-5.3 3.9-6.2.4-1.1-4.5-3.3-7.3-6-7.3-1.3 0-2.7.4-3 1-.3.5-1.5 1-2.6 1-1 0-2.4.9-3.1 1.9-1.1 1.8-1.4 1.8-3.5.4-1.4-1-3.4-1.3-5.2-1-2.3.5-3.2.1-4.4-1.6-1.4-2.1-1.6-2.1-4.4-.5-1.6.9-4.7 1.7-6.9 1.7h-6.9c-7.1.2-10.3-.9-11.4-4-1-2.9-1.3-3-6.3-2.9-5.7.2-13.5-1.7-15.6-3.7-.7-.7-2.6-1.3-4.2-1.3s-5.3-.6-8.2-1.3c-8-2-44.7-.5-45.5 1.8-1.2 3.4-3.1 6.1-5.1 7.1-1.3.6-2.8 1.8-3.5 2.7-1 1.4-1.8 1.4-5 .4-3.2-1-3.7-1.6-3.7-4.2 0-1.6.5-4.7 1.1-6.9 1.6-5.8.6-7.9-5.6-11.7-3-1.8-5.5-4-5.5-4.9 0-4.5 8.1-12 12.9-12 1.1 0 3.4-1.3 5.1-2.8l3-2.8-1.4-7.7c-.8-4.2-1.2-9.2-.9-11.1.4-2.5 0-4.4-1.2-6.2-2.1-3.3-4.1-10.3-5-17.4-.3-3-.9-6.3-1.1-7.3-.5-1.5.3-1.7 7-1.7 7.4 0 7.6.1 7.6 2.5v2.5h28.7c17.9 0 28.3-.4 27.7-.9-.5-.6-3.1-1.2-5.9-1.4l-5-.3 5.8-.2c4-.1 5.6-.6 5.1-1.3-.4-.7-2.5-.9-5.5-.7-2.7.3-4.9.1-4.9-.3 0-.9 7-1.3 15.8-.9 2.4.1 4.2-.3 4.2-.9 0-.7-3.5-1.1-10-1.1-6 0-10-.4-10-1s13.7-1 39-1 39 .4 39 1-7 1-19 1c-11.6 0-19 .4-19 1s5.5.9 13.8.9c21.6-.1 24.2 0 24.2 1 0 .4-2.2.6-5 .3-3.3-.3-5-.1-5 .7 0 .7 2 1.1 5.2 1.1 2.8 0 4.9.3 4.6.6-.4.3-7 .6-14.7.6-7.8 0-14.1.4-14.1.9s16.1.9 38 .9h38V94l-24.2-.2c-15.4-.2-24.3-.7-24.3-1.3 0-.6 8.8-1.1 23.8-1.3L200 91v-7.5c0-6-.3-7.5-1.5-7.5-.8 0-1.5.4-1.5 1s-3.7 1-9 1-9-.4-9-1-.7-1-1.5-1-1.5.4-1.5 1-3.7 1-9 1-9-.4-9-1-.7-1-1.5-1-1.5.4-1.5 1c0 .5-1.8 1-4.1 1h-4l.2 5.7.3 5.8-7.5.7c-18.1 1.5-57.2.7-58.5-1.3-.3-.5 0-.9.6-.9.7 0 1-1.7.8-4.8-.3-4.4-.5-4.7-3.3-5-1.6-.2-3.6-.9-4.3-1.4-.9-.8-1.6-.8-2.4 0-1.6 1.6-5.8 1.5-5.8-.1 0-.6.9-2.6 1.9-4.3 1-1.7 2.6-5.5 3.4-8.5 1.6-5.3 1.8-5.5 5.9-6.5 3.6-.8 4.3-1.4 5-4.2.6-2.2 1.4-3.2 2.8-3.2 8 0 13.1-8.9 8-14-3.3-3.3-2.5-6.5 2.9-12 4.9-5 5-5.1 9.8-4.5 6.5.9 9.9-.6 12-5.2 1.5-3.4 7-10.3 8.2-10.3.2 0 1.3.7 2.2 1.6zM77.5 92c.4.6-3.3 1-10.5 1s-10.9-.4-10.5-1c.3-.6 5-1 10.5-1s10.2.4 10.5 1z" fill="currentColor"/>
            <path d="M170.5 45.8c-1.6 1-3.6 2.6-4.4 3.5-1.2 1.6-.3 1.7 11.8 1.7 7.4 0 13.1-.4 13.1-.9s-1.4-2-3.2-3.2c-4.4-3.2-13.2-3.7-17.3-1.1zM162 61.4c0 1.4.4 3.6 1 5l1 2.6h28.9l1-3.8c1.9-6.5 2.6-6.2-15.4-6.2H162v2.4zM86 80.6c0 5.6.2 6.5 1.6 6 .9-.3 2-.6 2.5-.6s.9-2.7.9-6c0-5.7-.1-6-2.5-6s-2.5.2-2.5 6.6zM95 79.1v5.1l3.3-.6c1.7-.4 4.7-1 6.5-1.3 3-.5 3.2-.8 3.2-4.4V74H95v5.1zM112.2 77.7c.2 3.1.7 3.9 2.6 4.1 2 .3 2.2-.1 2.2-3.7 0-3.7-.2-4.1-2.6-4.1-2.3 0-2.5.3-2.2 3.7zM121 77.7v3.8l6.5 1.5 6.5 1.6V74h-13v3.7zM138 80c0 3.3.4 6 .9 6s1.6.3 2.5.6c1.4.5 1.6-.4 1.6-6 0-6.4-.1-6.6-2.5-6.6s-2.5.3-2.5 6zM97 101c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM107 101c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM88.5 104c-.4.6 1 1 3.5 1s3.9-.4 3.5-1c-.3-.6-1.9-1-3.5-1s-3.2.4-3.5 1zM97.5 104c-.4.6 1 1 3.5 1s3.9-.4 3.5-1c-.3-.6-1.9-1-3.5-1s-3.2.4-3.5 1zM107 104c0 .5 1.6 1 3.5 1s3.5-.5 3.5-1c0-.6-1.6-1-3.5-1s-3.5.4-3.5 1zM116.5 104c-.4.6 1 1 3.5 1s3.9-.4 3.5-1c-.3-.6-1.9-1-3.5-1s-3.2.4-3.5 1zM125.5 104c-.4.6 1 1 3.4 1 2.3 0 4.1-.5 4.1-1 0-.6-1.5-1-3.4-1s-3.8.4-4.1 1zM134.5 104c-.4.6 1.2 1 4 1s4.4-.4 4-1c-.3-.6-2.1-1-4-1s-3.7.4-4 1zM88 107c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM97 107c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM107 107c0 .5 1.8 1 4.1 1 2.4 0 3.8-.4 3.4-1-.3-.6-2.2-1-4.1-1-1.9 0-3.4.4-3.4 1zM116 107c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM109.9 113.7l-79.7.3-1.6 2.5L27 119h26c25.3 0 26 .1 26 2 0 1.3.7 2 2 2 1.6 0 2-.7 2-3.5V116h10v3.5c0 4.6 2.7 4.9 3.2.2.3-3.1.4-3.2 5.6-3.5l5.2-.3v3.5c0 2.5.4 3.6 1.5 3.6 1 0 1.5-1.1 1.5-3.5V116h11v3.5c0 2.4.5 3.5 1.5 3.5s1.5-1.1 1.5-3.5V116h10v3.5c0 2.8.4 3.5 2 3.5s2-.7 2-3.5V116h10v3.5c0 3.8 1.4 4.7 2.3 1.5.5-1.9 1.4-2 26.6-2 14.4 0 26.1-.3 26.1-.8-.1-.4-.9-1.7-1.9-3-1.6-1.8-2.8-2.2-6.8-2-2.6.2-40.6.4-84.4.5z" fill="currentColor"/>
            <path d="M29 128.5v7.2l17.5.1H64l-.3-7.2-.2-7.1-17.2-.1-17.3-.2v7.3zm5.5-.5c.3.5-.1 1-1 1s-1.3-.5-1-1c.3-.6.8-1 1-1 .2 0 .7.4 1 1zm6.5 0c0 .5-.4 1-1 1-.5 0-1-.5-1-1 0-.6.5-1 1-1 .6 0 1 .4 1 1zm6 0c0 .5-.4 1-1 1-.5 0-1-.5-1-1 0-.6.5-1 1-1 .6 0 1 .4 1 1zm6 0c0 .5-.4 1-1 1-.5 0-1-.5-1-1 0-.6.5-1 1-1 .6 0 1 .4 1 1zm6 0c0 .5-.5 1-1.1 1-.5 0-.7-.5-.4-1 .3-.6.8-1 1.1-1 .2 0 .4.4.4 1zM65.1 128.5c0 7.3.1 7.5 2.5 7.5 2.3 0 2.4-.2 2.4-7.5s-.1-7.5-2.4-7.5c-2.4 0-2.5.2-2.5 7.5zM72 128.5c0 6.8.2 7.5 2 7.5s2-.7 2-7.5-.2-7.5-2-7.5-2 .7-2 7.5zM153 128.4c0 7.4.1 7.6 2.5 7.6s2.5-.1 2.2-7.3c-.2-6.6-.4-7.2-2.4-7.5-2.2-.3-2.3 0-2.3 7.2zM159 128.5v7.3h20.9l21-.1v-14.3l-21-.1-20.9-.1v7.3zm6 .1c0 .8-.5 1.2-1 .9-.6-.4-.8-1.1-.5-1.6.9-1.4 1.5-1.1 1.5.7zm6.5-.6c.3.5-.1 1-1 1s-1.3-.5-1-1c.3-.6.8-1 1-1 .2 0 .7.4 1 1zm6 0c.3.5.1 1-.4 1-.6 0-1.1-.5-1.1-1 0-.6.2-1 .4-1 .3 0 .8.4 1.1 1zm6.5 0c0 .5-.4 1-1 1-.5 0-1-.5-1-1 0-.6.5-1 1-1 .6 0 1 .4 1 1zm6 0c0 .5-.4 1-1 1-.5 0-1-.5-1-1 0-.6.5-1 1-1 .6 0 1 .4 1 1zm6.5 0c.3.5-.1 1-1 1s-1.3-.5-1-1c.3-.6.8-1 1-1 .2 0 .7.4 1 1zM79.8 126.2c.9.9 1.5.9 2.4 0 .9-.9.7-1.2-1.2-1.2s-2.1.3-1.2 1.2zM93 126c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM107 126c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM121 126c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM134.8 126.2c.9.9 1.5.9 2.4 0 .9-.9.7-1.2-1.2-1.2s-2.1.3-1.2 1.2zM148 126c0 .5.5 1 1 1 .6 0 1-.5 1-1 0-.6-.4-1-1-1-.5 0-1 .4-1 1zM79.5 129c.3.5 2.2 1 4.1 1 1.9 0 3.4-.5 3.4-1 0-.6-1.8-1-4.1-1-2.4 0-3.8.4-3.4 1zM88 129c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM97 129c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM107 129c0 .5 1.5 1 3.4 1s3.8-.5 4.1-1c.4-.6-1-1-3.4-1-2.3 0-4.1.4-4.1 1zM116 129c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM125 129c0 .5 1.8 1 4 1s4-.5 4-1c0-.6-1.8-1-4-1s-4 .4-4 1zM134.5 129c.7 1.2 15.5 1.2 15.5-.1 0-.5-3.6-.9-8.1-.9-4.9 0-7.8.4-7.4 1zM79.4 133.9c-.2.2-.4 3.3-.4 6.8 0 5.6.2 6.3 2 6.3 1.6 0 2-.7 2-3.5V140h10v3.5c0 4.6 2.7 4.9 3.2.2.3-3.1.4-3.2 5.6-3.5l5.2-.3v3.5c0 2.5.4 3.6 1.5 3.6 1 0 1.5-1.1 1.5-3.5V140h11v3.5c0 2.4.5 3.5 1.5 3.5s1.5-1.1 1.5-3.5V140h10v3.5c0 2.8.4 3.5 2 3.5s2-.7 2-3.5V140h10v3.5c0 1.9.5 3.5 1 3.5.6 0 1-2.9 1-6.8v-6.7h-35.1c-19.3 0-35.3.2-35.5.4zM29 143.9v2.9l17.3-.1 17.2-.2.3-2.8.3-2.7H29v2.9zM65 144c0 2.5.4 3 2.5 3s2.5-.5 2.5-3-.4-3-2.5-3-2.5.5-2.5 3zM72 144c0 2.3.4 3 2 3s2-.7 2-3-.4-3-2-3-2 .7-2 3zM153 144.1c0 2.6.3 3 2.3 2.7 1.6-.2 2.3-1.1 2.5-3.1.3-2.3 0-2.7-2.2-2.7s-2.6.4-2.6 3.1zM159 143.9v2.8h42V141h-42v2.9zM29 151.5v3.2l17.6.1h17.5l-.3-3.2-.3-3.1-17.2-.2-17.3-.1v3.3zM65 151.5c0 3.1.3 3.5 2.5 3.5s2.5-.4 2.5-3.5-.3-3.5-2.5-3.5-2.5.4-2.5 3.5zM72 151.5c0 2.8.4 3.5 2 3.5s2-.7 2-3.5-.4-3.5-2-3.5-2 .7-2 3.5zM153 151.5c0 3.2.3 3.6 2.3 3.3 1.7-.2 2.2-1 2.2-3.3s-.5-3.1-2.2-3.3c-2-.3-2.3.1-2.3 3.3zM159 151.5v3.3h42v-6.6h-42v3.3zM79.8 150.2c.9.9 1.5.9 2.4 0 .9-.9.7-1.2-1.2-1.2s-2.1.3-1.2 1.2zM93 150c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM107 150c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM121 150c0 .5.7 1 1.5 1s1.5-.5 1.5-1c0-.6-.7-1-1.5-1s-1.5.4-1.5 1zM134.5 150c.3.5 1.3 1 2.1 1s1.4-.5 1.4-1c0-.6-.9-1-2.1-1-1.1 0-1.7.4-1.4 1zM148 150c0 .5.5 1 1 1 .6 0 1-.5 1-1 0-.6-.4-1-1-1-.5 0-1 .4-1 1zM148.8 155.5c-.4.4-16.2.7-35.2.7-29.2 0-34.6.2-34.6 1.4s-4 1.4-24.5 1.4H30v19h21.5c18.4 0 21.5-.2 21.5-1.5s5.3-1.5 42-1.5 42 .2 42 1.5 3.1 1.5 22 1.5h22v-19h-24.8c-24.2 0-24.9-.1-25.8-2.1-.5-1.1-1.2-1.7-1.6-1.4zM92.5 165v4.5l-4.7.3-4.8.3v-4.4c0-2.4.3-4.7.7-5.1.4-.4 2.5-.6 4.8-.4l4 .3v4.5zm13.5 0v5h-9v-10h9v5zm14 0v5h-9v-10h9v5zm14 0v5h-9v-10h9v5zm13 .1v5l-4.2-.3c-4.1-.3-4.3-.5-4.6-3.6-.5-5.2.3-6.2 4.8-6.2h4v5.1zM46.8 46.2c-7.1 4.1-6 4.8 8.3 4.8 14.2 0 15.2-.5 8.9-4.8-4.4-3-12.1-3-17.2 0z" fill="currentColor"/>
          </svg>
          <span>БЕЛГИДРОМЕТ</span>
        </a>
        <button class="button-back" type="button">
          Назад
        </button>
      </div>
    </header>
    <main class="main">
      <div class="main__container container" :style="maxHeight">
        <slot></slot>
      </div>
    </main>
    <footer class="footer">
      <div class="footer__container container">
        Гидрометеорология. В будущее с новыми технологиями
      </div>
    </footer>
  </div>
</template>

<style lang="scss">
.page-layout {
  display: grid;
  grid-template-rows: auto 1fr auto;
  height: 100dvh;
  background-color: var(--darkenTheme);
  overflow: hidden;
}
.header {
  background-color: var(--darkTheme);
  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
  }
}
.main {
  align-content: center;
  &__container {
    height: 100%;
  }
}
.footer {
  background-color: var(--darkTheme);
  color: var(--lightTheme);
  text-align: center;
  &__container {
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 10px;
    padding-bottom: 10px;
  }
}
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
.logo-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  color: var(--lightTheme);
  transition: color .3s ease;
  text-decoration: none;
  @media (hover: hover) {
    &:hover {
      color: var(--primaryTheme);
    }
  }
}
.button-back {
  font-size: 15px;
  font-weight: 600;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  color: var(--darkenTheme);
  background-color: var(--primaryTheme);
  cursor: pointer;
  transition: color .3s ease, background-color .3s ease;
  @media (hover: hover) {
    &:hover {
      color: var(--darkenTheme);
      background-color: var(--lightTheme);
    }
  }
}
</style>
