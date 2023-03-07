<script lang="ts">
import TheCarousel from '../components/Home/TheCarousel.vue'
import TheFilters from '../components/Home/TheFilters/TheFilters.vue'
import TheItems from '../components/Home/TheItems/TheItems.vue'

export default {
  components: {
    TheCarousel,
    TheFilters,
    TheItems
  }
}
</script>

<template>
  <TheCarousel />
  <div className="filter-items">
    <TheFilters />
    <TheItems />
  </div>
</template>

<style scoped>
.filter-items {
  display: flex;
  margin-top: 30px;
}
</style>
