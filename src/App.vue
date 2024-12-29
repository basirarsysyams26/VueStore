<template>
  <div id="app">
    <!-- Menambahkan NavbarApp di sini -->
    <NavbarApp />

    <router-view />
  </div>
</template>

<script>
// Mengimpor NavbarApp.vue yang sudah Anda buat
import NavbarApp from "./components/NavbarApp.vue";

export default {
  components: {
    NavbarApp, // Mendaftarkan NavbarApp sebagai komponen lokal
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

#app {
  margin: auto;
  max-width: 800px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* Menambahkan styling global jika diperlukan */
</style>
