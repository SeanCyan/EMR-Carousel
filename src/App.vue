<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'


const emails = [
 "lerbolario", "fairmont", "tussauds"
]


const random = Math.floor(Math.random() * emails.length);



const images = [
 {
  id: 1,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/loccitaneEMR.png`
 },
 {
  id: 2,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/fairmontEMR.png`
 },
 {
  id: 3,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/lycaEMR.png`
 },
 {
  id: 4,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/eeEMR.png`
 },
 {
  id: 5,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/dubaiEMR.png`
 },
 {
  id: 6,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/porscheEMR.png`
 },
 {
  id: 7,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/smithEMR.png`
 },
 {
  id: 8,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/intiminaEMR.png`
 },
 {
  id: 9,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/tussaudsEMR.png`
 },
 {
  id: 10,
  url: `https://raw.githubusercontent.com/SeanCyan/Portfolio/refs/heads/master/img/EMR/lerbolarioEMR.png`
 }
]


console.log(images);


const config = {
 itemsToShow: 5,
 gap: 40,
 wrapAround: true,


  // 'breakpointMode' determines how the carousel breakpoints are calculated
 // Acceptable values: 'viewport' (default) | 'carousel'
 // 'viewport' - breakpoints are based on the viewport width
 // 'carousel' - breakpoints are based on the carousel width
 breakpointMode: 'carousel',


 // Breakpoints are mobile-first
 // Any settings not specified will fall back to the carousel's default settings
 breakpoints: {
  // 300px and up
  300: {
   itemsToShow: 1,
   snapAlign: 'center',
  },
    // 400px and up
    400: {
   itemsToShow: 1,
   snapAlign: 'center',
  },
  // 500px and up
  500: {
   itemsToShow: 1,
   snapAlign: 'center',
  },
      // 700px and up
      700: {
   itemsToShow: 1,
   snapAlign: 'center',
  },
      // 700px and up
      800: {
   itemsToShow: 2,
   snapAlign: 'center',
  },
    // 900px and up
    1025: {
   itemsToShow: 5,
   snapAlign: 'center',
  },
 },
}
</script>


<template>
 <Carousel v-bind="config">
  <Slide v-for="image in images" :key="image.id">
   <img :src="image.url" alt="image" />
  </Slide>


  <template #addons>
   <Navigation />
  </template>
 </Carousel>
</template>


<style>
:root {
 background-color: #ffffff;
}


.carousel {
 --vc-nav-background: rgba(255, 255, 255, 0.7);
 --vc-nav-border-radius: 100%;
 width:100vw;
 margin:0 auto;
}


img {
 border-radius: 20px;
 width: auto;
 height: 90vh;
 object-fit: contain;
 -webkit-box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
-moz-box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
box-shadow: 0px 0px 32px -8px rgba(0,0,0,0.2);
margin-top: 25px;margin-bottom:10px;
}
.carousel__next,
.carousel__prev {
 background: rgba(0, 0, 0, 0.3);
 border-radius: 50%;
 width: 40px;
 height: 40px;
 color: white;
 margin: 0 10px;
}
</style>

