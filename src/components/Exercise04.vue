<template>
    <div>
        <div :class="{ active: isActive }" :style="{ backgroundColor: backgroundColor }">
            Block
        </div>
        <p>isActive={{ isActive }}</p>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isActive = ref(true)
const backgroundColor = ref('blue')
</script>

<style scoped>
div {
    width: 200px;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 10px;
}

.active {
    color: #fff;
}
</style>