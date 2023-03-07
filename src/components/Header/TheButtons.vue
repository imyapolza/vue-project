<script lang="ts">
export default {};
</script>

<template>
  <div class="header-buttons">
    <div class="search-cart-buttons">
      <button>
        <img src="assets/images/header/search.svg" alt="search" />
      </button>
      <button>
        <img src="assets/images/header/cart.svg" alt="cart" />
      </button>
    </div>
    <button class="button-logout">
      <img src="assets/images/header/logout.svg" alt="logout" />
      <span class="login-text">Login</span>
    </button>
  </div>
</template>

<style scoped>
.header-buttons {
  display: flex;
  align-items: center;
}

.search-cart-buttons {
  margin-right: 35px;
}

.search-cart-buttons :first-child {
  margin-right: 15px;
}

.button-logout {
  background: #46a358;
  border-radius: 6px;
  width: 100px;
  height: 35px;
  color: #ffffff;
  font-size: 16px;
  font-family: "Cera Pro";
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
}

.login-text {
  margin-left: 4px;
  font-weight: 300;
}
</style>
