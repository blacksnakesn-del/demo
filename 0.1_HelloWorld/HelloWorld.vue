<script setup>

const message = "Teksi birique!"
 
</script>

<template>
  <section class="card">

    <h1>0.1_HelloWorld</h1>
    <p>Premiers composant vue()</p>
    <div class="box">
        <strong>Message: {{ message.toUpperCase()}}</strong>
    </div>

  </section>
</template>



<style scoped>

.card {
    padding: 16px;
    border: 1px solid #eee;
    border-radius: 20px;
}

.box {
    margin-top: 10px;
    padding: 12px;
    border: 1px dashed #ccc;
    border-radius: 10px;
}

</style>