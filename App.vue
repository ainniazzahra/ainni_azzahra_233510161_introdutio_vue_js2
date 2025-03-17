<script setup>
import { ref } from 'vue';

const message = ref("Halo!");
const counter = ref(0);

const increment = () => {
  counter.value++;
};

const showMessage = ref(true);
</script>

<template>
  <div class="container">
    <h1>{{ message }}</h1>
    <input v-model="message" placeholder="Ubah teks di sini" class="input-box" />
    <button @click="increment" class="btn">Tambah</button>
    <p class="counter-text">Counter: {{ counter }}</p>
    <img :src="'https://tse3.mm.bing.net/th?id=OIP.A8m51bA9jptiPz6dWqSN-AHaF9&pid=Api&P=0&h=220'" :alt="'Gambar'" class="image" />

    <!-- 8. Menggunakan Conditional Rendering -->
    <div v-if="showMessage" class="message-box">
      <p>Nama: Bacharuddin Jusuf Habibie</p>
      <p> Lahir: Pare-pare, Sulawesi selatan, 25 juni 1936</p>
      <p> presiden republik indonesia (1998-1999)</p>
    </div>
    <button @click="showMessage = !showMessage" class="btn toggle-btn">
     Pesan
    </button>
  </div>
</template>

<style scoped>
.container {
  text-align: center;
  margin-top: 50px;
  padding: 20px;
  border-radius: 10px;
  background-color: #f4f4f4;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

h1 {
  color: #333;
}

.input-box {
  margin-top: 10px;
  padding: 8px;
  width: 80%;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.btn {
  margin: 10px;
  padding: 10px 15px;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color: aqua;
  color: white;
}

.btn:hover {
  background-color: #116280;
}

.counter-text {
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

.image {
  margin-top: 10px;
  width: 200px;
  height: auto;
  border-radius: 10px;
  border: 2px solid #ddd;
}

.message-box {
  margin-top: 15px;
  background-color: #e3f2fd;
  padding: 10px;
  border-radius: 5px;
}

.toggle-btn {
  background-color: #28a745;
}

.toggle-btn:hover {
  background-color: #218838;
}
</style>