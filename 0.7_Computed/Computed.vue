<script setup>
import { computed, reactive, ref } from 'vue';


const cart = reactive([
    {nom:'Cahier', prix: 500, quantite:50},
    {nom:'Stylo', prix: 200, quantite:20},
    {nom:'Protege', prix: 50, quantite:200},
    {nom:'Gome', prix: 100, quantite:20},
    {nom:'Livre', prix: 2000, quantite:100},
])

const total = computed(function() {
    return cart.reduce((a, s) => a+s.prix*s.quantite, 0)
})

 

</script>

<template>
  <section class="card">
    <h2>11 - computed()</h2>

    <ul>
      <li v-for="item in cart" :key="item.nom">
       {{ item.nom }} : {{ item.prix }} × {{ item.quantite }} -> {{ item.prix * item.quantite }} FCFA
      </li>
    </ul>

    <h3>Total : {{ total }} FCFA</h3>

    <p class="note">
      Le total se met à jour automatiquement.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.note { margin-top:8px; color:#555; }
</style>