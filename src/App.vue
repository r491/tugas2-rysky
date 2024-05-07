<script setup>
import { ref } from 'vue'

const titleclass = ref('title')
const dynamicId = ref('title')
const count = ref(0)
const Pesan = ref('')

function increment() {
  count.value++
}
</script>

<template>
  <img src="/download.jpeg" alt="">
  <div>
    <p v-bind:class='titleclass'> PT Toys Games Indonesia (Toys Kingdom) yang didirikan tahun 2010 menyediakan lebih dari 23.000 koleksi lengkap mainan dan hobi untuk segala usia, yang terbagi menjadi enam kategori, yaitu babies, girls, boys, education, family fun, dan outdoor</p><br>
<p class="text">Nama Mainan: {{ Pesan }}</p>
<input v-model="Pesan" placeholder="Isi disini" />
  </div>
  <br>
<button @click="increment">Jumlah {{ count }}</button>
</template>

<style>

img {
 background-position: center; 
}
.title{
  color: rgb(255, 255, 255);
}
.text {
  color: rgb(255, 255, 255);
}
#title {
  color: rgb(255, 255, 255);
}
</style>