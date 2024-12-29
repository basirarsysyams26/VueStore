<template>
  <div id="nav-bar">
    <router-link :to="{ name: 'product' }" id="products-link"
      >VueStore</router-link
    >
    <router-link :to="{ name: 'cart' }" id="cart-link">
      <button>Cart</button>
    </router-link>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#nav-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #ddd;
  height: 75px;
  width: 100%;
  padding: 0 16px;
}

#products-link {
  color: #41b883;
  font-size: 22px;
  text-decoration: none;
}

button {
  background-color: #41b883;
  color: white;
  font-size: 16px;
  font-weight: bold;
  border-radius: 8px;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}
</style>
