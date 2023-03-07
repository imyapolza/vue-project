<script lang="ts">
export default {
  name: 'ThePagination',
  props: {
    pages: Number
  }
}
</script>

<template>
  <div class="wrapper">
    <button
      v-for="(page, index) in pages"
      :key="index"
      class="page"
      :class="{ active: index === 0 }"
    >
      {{ page }}
    </button>
    <button class="page">
      <img class="next-arrow" src="@/assets/images/arrow.svg" alt="next arrow" />
    </button>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  justify-content: flex-end;
  margin: 100px 0;
  width: 100%;
}
.page {
  width: 35px;
  height: 35px;
  border: 1px solid #e5e5e5;
  border-radius: 4px;
  margin-right: 10px;
  font-size: 18px;
  font-family: 'Cera Pro';
  font-weight: 300;
}

.active {
  background: #46a358;
  border-radius: 4px;
  color: #ffffff;
  font-size: 18px;
  font-family: 'Cera Pro';
}

.next-arrow {
  transform: rotate(270deg);
}
</style>
