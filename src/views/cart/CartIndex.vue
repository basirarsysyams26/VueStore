<template>
  <div>
    <div id="page-wrap">
      <h1>Shopping Cart</h1>
      <div class="product-container" v-for="item in cartItems" :key="item.id">
        <img :src="item.imageUrl" alt="" class="product-image" />
        <div class="details-wrap">
          <h3>{{ item.name }}</h3>
          <p>Rp{{ item.price }}</p>
        </div>
        <div>
          <button class="remove-button">Remove</button>
        </div>
      </div>
      <h3 id="total-price">Total: Rp{{ totalPrice }}</h3>
      <button id="checkout-button">Checkout</button>
    </div>
  </div>
</template>

<script>
import { cartItems } from "@/data-seed";

export default {
  data() {
    return {
      cartItems,
    };
  },
  computed: {
    totalPrice() {
      return this.cartItems.reduce((sum, item) => sum + Number(item.price), 0);
    },
  },
};
</script>

<style scoped>
h1 {
  border-bottom: 1px solid #41b883;
  margin: 0;
  margin-top: 16px;
  padding: 16px;
}

#total-price {
  padding: 16px;
  text-align: right;
}

#checkout-button {
  width: 100%;
}

.product-container {
  align-items: center;
  border-bottom: 1px solid #ddd;
  display: flex;
  padding: 16px;
  width: 100%;
}

.product-image {
  flex: 1;
  height: 100px;
  max-width: 100px;
}

.details-wrap {
  padding: 0 16px;
  flex: 3;
}

.remove-button {
  flex: 1;
  margin: auto;
}
</style>
