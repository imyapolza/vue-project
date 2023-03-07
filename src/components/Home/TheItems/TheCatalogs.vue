<script lang="ts">
import { catalogs } from '../../../constants/home/items'

export default {
  name: 'TheCatalogs',
  data() {
    return {
      catalogs
    }
  }
}
</script>

<template>
  <ul class="catalogs">
    <li v-for="(catalog, index) in catalogs" :key="index" class="catalog">
      <button class="catalog-button" :class="{ 'catalog-button-active': index === 0 }">
        {{ catalog }}
      </button>
      <transition name="fade">
        <img
          v-show="index === 0"
          class="catalog-active"
          src="assets/images/active-line.png"
          alt="active-nav-line"
        />
      </transition>
    </li>
  </ul>
</template>

<style scoped>
ul > li:not(:first-child) {
  margin-right: 40px;
}
.catalogs,
.catalog {
  display: flex;
}

.catalog {
  position: relative;
}

.catalogs > li:not(:last-child) {
  margin-right: 40px;
}

.catalogs > button {
  font-weight: 300;
}

.catalog-button-active {
  color: #46a358;
}

.catalog-active {
  position: absolute;
  top: 25px;
  width: 100%;
  height: 3px;
}

.catalog-button {
  font-weight: 300;
}
</style>
