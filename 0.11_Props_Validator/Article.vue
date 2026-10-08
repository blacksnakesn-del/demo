<script setup>

defineProps({
    abdou:Object
})
// const prod = { id: 1, name: 'Stylo', price: 500 }

</script>

<template>

    <article class="card">
        <h3 class="name">{{ abdou.name }}</h3>
        <p class="price">{{ abdou.price.toLocaleString() }} FCFA</p>
        <p class="meta">ID: {{ abdou.id }}</p>
      </article>

</template>

<style scoped>

.card { padding: 14px; border: 1px solid #eee; border-radius: 12px; background: #fff; }
.name { margin: 0; font-size: 16px; }
.price { margin: 6px 0 0; font-weight: 700; }
.meta { margin: 6px 0 0; color: #666; font-size: 12px; }

</style>