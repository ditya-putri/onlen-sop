<script setup>
import ProductCard from '../components/ProductCard.vue'
 
const daftarProduk = [
  { id: 1, nama: 'seblak', harga: 5000000, gambar: 
'https://cdn.idntimes.com/content-images/community/2021/02/fromandroid-2a60232ed16b5f37d2f27e1af00ed96f.jpg' },
  { id: 2, nama: 'bakso', harga: 10000000, gambar: 
'https://cdn.idntimes.com/content-images/community/2019/06/774b2584-2da7-429e-b3aa-8a4a4561b974-225f13c2e62b17ee20e26d2b520f33fb.jpeg' },
  { id: 3, nama: 'cilok', harga: 5000000, gambar: 
'https://palpos.disway.id/upload/6e68ca59e89194824b3aa7dc598da23a.jpg' },
]
</script>
 
<template>
  <main>
    <h1>Produk Kami</h1>
    <div class="grid">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />
    </div>
  </main>
</template>
 
<style scoped>
.grid {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}
button { 
  margin-top: 8px; 
  padding: 6px 12px; 
  border: none; 
  border-radius: 6px; 
  background: #2E75B6; 
  color: white; 
  cursor: pointer; 
} 
button:hover { background: #1F4E79; } 
</style>