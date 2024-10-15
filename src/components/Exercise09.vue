<template>
    <div>
        <p>Giá trị count: {{ count }}</p>
        <button @click="incrementCount">Tăng Count</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)

const incrementCount = () => {
    count.value++
}
</script>

<style scoped>
button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

p {
    font-size: 18px;
    font-weight: bold;
}
</style>