<script lang="ts">
export default {}
</script>

<template>
  <div class="wrapper">
    <img src="assets/images/main/items/1.png" alt="item image" />
    <h4 class="title">Barberton Daisy</h4>
    <span class="price">$119.00</span>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  width: 250px;
}

.title {
  font-family: 'Cera Pro';
  font-weight: 300;
  color: #3d3d3d;
  font-size: 17px;
  margin-bottom: 6px;
}

.price {
  font-family: 'Cera Pro';
  color: #46a358;
  font-weight: 700;
  font-size: 18px;
}
</style>
