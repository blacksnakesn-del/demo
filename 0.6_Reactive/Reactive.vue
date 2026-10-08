<script setup>
import { reactive, ref } from 'vue';


const info = reactive({nom:"Abdou", Telephone:769286371, Solde:12345})
const nbr = ref(0)
const montantAjouter = ref()


function ajouter(montant) {

    if(nbr.value < 10) {
        info.Solde += montant
        nbr.value++
    }
    
}

</script>

<template>
  <section class="card">
    <h2>09 - reactive()</h2>

    <div class="box">
      <p><strong>Nom :</strong> {{info.nom}} </p>
      <p><strong>Téléphone :</strong> {{info.Telephone}} </p>
      <p><strong>Solde :</strong> {{info.Solde}} FCFA</p>
      <p><strong>Nombre Ajout: {{ nbr }}</strong></p>
    </div>

    <div class="actions">
      <button @click="ajouter(5000)">+5 000</button>
      <button @click="ajouter(10000)">+10 000</button>
      <input type="tel" placeholder="autre Montant" v-model="montantAjouter" @keyup.enter="ajouter(montantAjouter)">
      <button class="valider" @click="ajouter(montantAjouter)" :disabled="nbr >= 10">Valider</button>
    </div>

    <p class="note">
      <code>reactive()</code> est idéal pour les objets complexes.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; background: #ddd;}
.box { padding:12px; background:#fafafa; border-radius:10px; }
.actions { display:flex; gap:10px; margin-top:10px; }
button { padding:8px 10px; border:1px solid #ddd; border-radius:8px; }
.note { margin-top:8px; color:#555; }
.valider { background: rgb(121, 240, 121); }
</style>