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
  <img src="/logo.png" alt="">
  <div>
    <p v-bind:class='titleclass'> Cafe biasanya di desain dengan sangat menarik dan instagram-able supaya membuat tamu merasa nyaman dan betah berlama-lama di cafe.
Untuk menambah daya tarik, tidak jarang mereka membuat sebuah hiburan dengan menghadirkan sebuah live music untuk hari-hari libur atau weekend, yang bertujuan untuk menemani pengunjung bersantai dan berbincang dengan alunan musik yang di suguhkan.

Secara Harfiah cafe adalah minuman (kopi), dan berubah menjadi sebuah tempat yang menyediakan berbagai macam minuman dan bukan hanya kopi, terkadang minuman dengan kadar alkohol rendah ada dalam daftar menu.</p>
<p v-bind:id='dynamicId'> Sekarang Silahkan isi menu anda pada kolom dibawah</p><br>
<p class="text">Masukkan Menu: {{ Pesan }}</p>
<input v-model="Pesan" placeholder="Isi disini" />
  </div>
  <br>
<button @click="increment">Jumlah {{ count }}</button>
</template>

<style>
div {
  background-image: url('/img.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}
img {
 background-position: center; 
}
.title{
  color: black;
}
.text {
  color: black;
}
#title {
  color: rgb(0, 0, 0);
}
</style>