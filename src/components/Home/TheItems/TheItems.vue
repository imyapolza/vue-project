<script lang="ts">
import TheCatalogs from './TheCatalogs.vue'
import TheSort from './TheSort.vue'
import TheItem from './TheItem.vue'
import ThePagination from '../../Pagination/ThePagination.vue'

export default {
  name: 'TheItems',
  components: { TheCatalogs, TheSort, TheItem, ThePagination }
}
</script>

<template>
  <div className="main">
    <div class="catalogs-sort">
      <TheCatalogs />
      <TheSort />
    </div>
    <div class="items">
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
      <TheItem />
    </div>
    <ThePagination :pages="5" />
  </div>
</template>

<style scoped>
ul > li {
  margin-right: 37px;
}

.main {
  width: 100%;
}

.catalogs-sort {
  display: flex;
  width: 100%;
  align-items: flex-start;
  justify-content: space-between;
  margin-left: 50px;
  height: 23px;
  font-family: 'Cera Pro';
  font-weight: 300;
}

.items {
  margin-top: 30px;
  margin-left: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
