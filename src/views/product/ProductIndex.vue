<template>
  <div>
    <div id="page-wrap">
      <div id="grid-wrap">
        <div v-for="product in products" :key="product.id" class="product-item">
          <img :src="product.imageUrl" alt="" />
          <h3 class="product-name">{{ product.name }}</h3>
          <p class="product-price">Rp{{ product.price }}</p>

          <!-- Menutup tag button dengan benar -->
          <router-link
            :to="{ name: 'product-detail', params: { id: product.id } }"
          >
            <button>Detail</button>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import { products } from "../../data-seed";
import { products } from "@/data-seed";

export default {
  data() {
    return {
      products,
    };
  },
};
</script>

<style scoped>
#grid-wrap {
  display: grid; /* Ganti ke grid layout */
  grid-template-columns: repeat(3, 1fr); /* Membuat 3 kolom */
  gap: 16px; /* Spasi antar item */
  margin-top: 16px;
}

.product-item {
  align-items: center;
  border-radius: 8px;
  box-shadow: 0px 2px 5px #888;
  display: flex;
  flex-direction: column;
  padding: 20px;
  position: relative;
  background-color: white; /* Menambahkan background agar lebih terlihat */
}

.product-name {
  margin-bottom: 0;
}

img {
  height: 200px;
  width: 200px;
  border-radius: 5%;
}

button {
  width: 100%;
}
</style>
