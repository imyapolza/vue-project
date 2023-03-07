<script lang="ts">
import { categories } from '../../../constants/home/categories'

export default {
  name: 'TheCategories',
  data() {
    return {
      categories
    }
  }
}
</script>

<template>
  <h3 class="title">Categories</h3>
  <ul class="list">
    <li v-for="({ category, count }, index) in categories" :key="index" class="category">
      <button class="button" :class="{ active: index === 0 }">
        <span class="category">{{ category }}</span>
        <span class="count">({{ count }})</span>
      </button>
    </li>
  </ul>
</template>

<style scoped>
span {
  display: inline-block;
}
.title {
  font-family: 'Cera Pro';
  font-weight: 500;
  font-size: 18px;
}

.list {
  margin-top: 20px;
  margin-left: 12px;
  font-family: 'Cera Pro';
  font-weight: 300;
}

.category:not(:last-child) {
  margin-bottom: 12px;
}

.button {
  font-weight: 300;
  display: flex;
  width: 100%;
  justify-content: space-between;
}

.active {
  color: #46a358;
  font-weight: 500;
}
</style>
