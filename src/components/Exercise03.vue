<template>
    <div>
        <input type="text" :disabled="isDisable" placeholder="Cho phép nhập">
        <p>isDisable={{ isDisable }}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isDisable = ref(false)
</script>

<style scoped>
input {
    padding: 5px;
    margin-bottom: 10px;
}
</style>