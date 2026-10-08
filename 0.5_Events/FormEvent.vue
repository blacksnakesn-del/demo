<script setup>
import { ref } from 'vue';


const nom = ref('')
const tel = ref('')
const tableau = ref([])

function addTableau() {
    if(!nom.value.trim() || !tel.value.trim()) return;
    
    tableau.value.unshift({
        id: crypto.randomUUID(),
        nom:nom.value,
        tel:tel.value
    })
    nom.value = "",
    tel.value = ""
}

function reset() {
    tableau.value = []
}
 
</script>

<template>

    <div class="parent">

        <div class="fille">
            <form action="#" type="submit" @submit.prevent="addTableau">
                <input type="text" placeholder="Nom Complet" v-model="nom">
                <input type="" placeholder="tel" v-model="tel">
                <button>Ajouter</button>
                <button class="reset" @click="reset">Reset</button>
            </form>
        </div>

        <div class="tableau">
            <table>
                <thead>
                    <tr>Nom Complet</tr>
                    <tr>Telephoone</tr>
                </thead>
                <tbody>
                    <tr><td>{{ tableau.nom }}</td></tr>
                    <tr><td>{{ tableau.tel }}</td></tr>
                </tbody>
            </table>
        </div>
         
    </div>
  
</template>

<style scoped>

.parent {
    background: whitesmoke;
    border: 1px solid rgb(255, 255, 255);
    padding: 12px;
    border-radius: 5px;
}

.fille {
    gap: 10px;
    
}

input {
    padding: 10px;
    margin: 10px 10px;
}

button {
    padding: 10px;
    background: rgb(151, 240, 151);
}

.reset {
    background: rgb(240, 119, 119);
    margin-left: 5px;
}

</style>