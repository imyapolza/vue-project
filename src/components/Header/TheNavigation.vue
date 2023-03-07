<script lang="ts">
import { navItems } from '../../constants/header/navigation'

export default {
  name: 'TheNavigation',
  data() {
    return {
      navItems
    }
  },
  computed: {
    currentRouteName() {
      return this.$route.path
    }
  }
}
</script>

<template>
  <nav class="navigation">
    <RouterLink v-for="({ title, to }, index) in navItems" :key="index" :to="to" class="nav-item">
      <span>{{ title }}</span>
      <transition name="fade">
        <img
          v-show="to === currentRouteName"
          class="nav-active"
          src="@/assets/images/active-line.png"
          alt="active-nav-line"
        />
      </transition>
    </RouterLink>
  </nav>
</template>

<style scoped>
.navigation {
  display: flex;
  align-items: center;
}

.nav-item {
  display: flex;
  height: 190%;
  align-items: center;
  position: relative;
  font-family: 'Cera Pro';
  color: #3d3d3d;
  font-weight: 300;
  font-size: 16px;
}

.nav-item:not(:last-child) {
  margin-right: 50px;
}

.nav-active {
  position: absolute;
  top: 72px;
  width: 100%;
  height: 3px;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}

.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
