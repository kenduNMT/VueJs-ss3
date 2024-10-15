<template>
    <button @click="handleClick('Rikkei Academy')">Get param</button>
</template>

<script setup lang="ts">
function handleClick(message: string) {
    console.log(message)
}
</script>

<style scoped>

</style>