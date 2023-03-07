<script lang="ts">
import TheNavigation from "./TheNavigation.vue";
import TheButtons from "./TheButtons.vue";

export default {
  components: {
    TheNavigation,
    TheButtons,
  },
};
</script>

<template>
  <header class="header">
    <RouterLink to="/">
      <img src="assets/images/header/logo.svg" alt="logo" />
    </RouterLink>

    <TheNavigation />
    <TheButtons />
  </header>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  border-bottom: 0.3px solid rgba(70, 163, 88, 0.5);
  padding-bottom: 18px;
}
</style>
