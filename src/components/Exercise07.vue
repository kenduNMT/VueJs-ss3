<template>
    <div>
        <input type="text" placeholder="Cho phép nhập">
        <form @submit.prevent="Block">
            <button>Submit</button>
        </form>
    </div>
</template>

<script setup lang="ts">
function Block() {
    console.log("Form submission prevented")
}
</script>

<style scoped>
input {
    padding: 5px;
    margin-bottom: 10px;
}
</style>