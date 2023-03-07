<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation
  }
}
</script>

<template lang="">
  <carousel class="carousel" :items-to-show="1" :autoplay="3000" :wrap-around="true">
    <slide v-for="slide in 3" :key="slide">
      <section class="section">
        <div class="left">
          <div>
            <h2 class="h2">Welcome to GreenShop</h2>
            <h1 class="h1">Let’s Make a Better <span class="h1-planet">Planet</span></h1>
            <span class="description"
              >We are an online plant shop offering a wide range of cheap and trendy plants. Use our
              plants to create an unique Urban Jungle. Order your favorite plants!</span
            >
          </div>

          <button class="shop-button">SHOP NOW</button>
        </div>

        <img src="@/assets/images/main/plant.svg" alt="plant" />
      </section>
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>

<style scoped>
.carousel {
  -webkit-user-select: none;
  -webkit-touch-callout: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.section {
  font-family: 'Cera Pro';
  display: flex;
  justify-content: space-between;
  background: linear-gradient(
    97.77deg,
    rgba(245, 245, 245, 0.5) -23.46%,
    rgba(245, 245, 245, 0.5) 107.51%
  );
  width: 100%;
  height: 450px;
  margin-top: 12px;
  margin-bottom: 26px;
}

.left {
  padding-top: 70px;
  margin-left: 45px;
}

.h2 {
  letter-spacing: 0.1em;
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 7px;
  text-transform: uppercase;
  opacity: 0.8;
}

.h1 {
  font-size: 70px;
  text-transform: uppercase;
  margin-bottom: 5px;
  width: 10em;
  opacity: 0.8;
}

.h1-planet {
  color: #46a358;
  line-height: 24px;
}

.description {
  font-size: 14px;
  color: #727272;
  width: 40em;
  display: inline-block;
  font-weight: 300;
  line-height: 24px;
}

.shop-button {
  background: #46a358;
  border-radius: 6px;
  width: 140px;
  height: 40px;
  text-transform: uppercase;
  color: #ffffff;
  margin-top: 65px;
}
</style>
