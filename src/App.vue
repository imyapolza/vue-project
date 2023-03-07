<script setup lang="ts">
import { RouterView } from "vue-router";
import TheHeader from "./components/Header/TheHeader.vue";
</script>

<template>
  <div className="root">
    <TheHeader />
    <RouterView />
  </div>
</template>

<style>
@import url("https://necolas.github.io/normalize.css/8.0.1/normalize.css");

.root {
  margin: 25px 120px 0 120px;
  height: 100%;
}

@font-face {
  font-family: "Cera Pro";
  src: local("Cera Pro Thin"), local("Cera Pro-Thin"),
    url("assets/fonts/CeraPro/CeraPro-Thin.woff2") format("woff2"),
    url("assets/fonts/CeraPro/CeraPro-Thin.woff") format("woff");
  font-style: normal;
  font-weight: 100;
}

@font-face {
  font-family: "Cera Pro";
  src: local("Cera Pro Regular"), local("Cera Pro-Regular"),
    url("assets/fonts/CeraPro/CeraPro-Regular.woff2") format("woff2"),
    url("assets/fonts/CeraPro/CeraPro-Regular.woff") format("woff");
  font-style: normal;
  font-weight: 300;
}

@font-face {
  font-family: "Cera Pro";
  src: local("Cera Pro Medium"), local("Cera Pro-Medium"),
    url("assets/fonts/CeraPro/CeraPro-Medium.woff2") format("woff2"),
    url("assets/fonts/CeraPro/CeraPro-Medium.woff") format("woff");
  font-style: normal;
  font-weight: 500;
}

@font-face {
  font-family: "Cera Pro";
  src: local("Cera Pro Black"), local("Cera Pro-Black"),
    url("assets/fonts/CeraPro/CeraPro-Black.woff") format("woff"),
    url("assets/fonts/CeraPro/CeraPro-Black.woff2") format("woff2");
  font-style: normal;
  font-weight: 900;
}

a {
  text-decoration: none;
}

button {
  background: 0;
  border: 0;
  margin: 0;
  padding: 0;
  cursor: pointer;
}

h1,
h2,
h3,
h4,
h5 {
  margin: 0;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}
</style>
