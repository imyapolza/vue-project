<script lang="ts">
export default {}
</script>

<template>
  <button class="sort">
    <span class="sort-param">Short by: Default Sorting</span>
    <img src="@/assets/images/arrow.svg" alt="arrow svg" />
  </button>
</template>

<style scoped>
.sort-param {
  font-weight: 300;
}

.sort-param:first-child {
  margin-right: 5px;
}

.sort {
  display: flex;
}
</style>
