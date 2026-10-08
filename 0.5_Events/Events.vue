<script setup>
import { ref } from 'vue';


const step = ref()
const compteur = ref(0)

function increment() {
    compteur.value += step.value
}

function reset() {
    compteur.value = 0
}

</script>

<template>

    <div class="mer">

        <div>
            <button @click="increment">Increment +</button>
            <button @click="reset">Reset</button>
        </div>

        <div>
            <input type="number" min="1" v-model="step" @keyup.enter="increment">
        </div>
        <h1>{{ compteur }}</h1>

    </div>
  
</template>

<style>

.mer {
    border: 1px solid black;
    padding: 20px;
    background: rgb(228, 225, 225);
    gap: 10px;
    border-radius: 12px;
}

</style>