<script setup>

const person = {nom : "Abdou", prenom : "Kebe"}
const role = "Developpeur Web Mobile"
const salaire = 1234567
const annee = new Date().getFullYear()
const prime = 0.50

</script>

<template>

    <div>

        <div class="info">
            <div>Nom: {{ person.nom }}</div>
            <div>Nom: {{ person.prenom }}</div>
            <div>Role: {{ role }}</div>
            <div>Saliare: {{ salaire }} <span>FCFA</span></div>
            <div>Annee: {{ annee }}</div>
            <div>Salaire Net: {{ salaire + salaire * prime }} <span>FCFA</span></div>
        </div>

    </div>
  
</template>


<style>

body {
    display: flex;
    align-items: center;
    justify-content: center;
}

.info {
    padding: 12px;
    border: 1px solid black;
    border-radius: 12px;
    margin: 10px;
    background: rgba(0, 0, 0, 0.2);
    box-shadow: 5px 5px rgba(0, 0, 0, 0.2);
}

div {
    padding: 10px;
    font-size: 2rem;
}

span {
    color: rgb(101, 175, 101);
}

</style>