<script setup>
import { ref } from 'vue';


const status = ref('')
// const input = ref('')
 
</script>

<template>

    <section class="card">

        <h2>0.4_Dynamique Attribut</h2>
        <div class="row">
            <span>Statut</span>
            <select v-model="status">
                <option value="success">Success</option>
                <option value="warning">Warning</option>
                <option value="danger">Danger</option>
            </select>

            <!-- <input type="text" value="input"> -->

            <p>{{ status }}</p>

        </div>

        <!-- <div>{{ input }}</div> -->

        <div class="bar" :style= "{ width:status==='danger' ? '10%' : status==='warning' ? '50%' : '100%' }"></div>

    </section>
  
</template>

<style scoped>

.card {
    padding: 16px;
    border: 1px solid #eee;
    border-radius: 20px;
}

.row {
    display: flex;
    gap: 12px;
    align-items: center;
}

.badge {
    padding: 6px 10px;
    border-radius: 999px;
    font-weight: 600;
    border: 1px solid #ddd;
}

.success { background: #e9f7ef; }
.warning { background: #fff7e6; }
.danger { background: #fdecea; }

.bar {
    height: 10px;
    border-radius: 999px;
    border: 1px solid #eee;
    background: #ddd;
    margin-top: 10px;
}

select {
    padding: 8px 10px;
    border: 1px solid #ddd;
    border-radius: 8px;
}

</style>