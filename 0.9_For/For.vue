<script setup>
import { ref } from 'vue';


const products = ref([
    {id:1, nom:'Cahier', prix: 500, quantite:50},
    {id:2, nom:'Stylo', prix: 200, quantite:20},
    {id:3, nom:'Protege', prix: 50, quantite:200},
    {id:4, nom:'Gome', prix: 100, quantite:20},
    {id:5, nom:'Livre', prix: 2000, quantite:100},
])

 const supprimer = (id) => {
    products = products.value.filter((p)=>p.id != id)
 }

</script>

<template>
  <section class="card">
    <h2>13 - Lists</h2>

    <ul>
      <li v-for="p in products" :key="p.id">
        {{p.nom}} - {{p.prix}} FCFA
        <button @click="supprimer">❌</button>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
li { display:flex; justify-content:space-between; width:250px; }
button { border:none; background:none; cursor:pointer; }
</style>