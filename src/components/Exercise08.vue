<template>
    <div>
        <input v-model="url" type="text" placeholder="Nhập đường dẫn">
        <button @click="checkUrl">Kiểm tra</button>
        <div v-if="showModal" class="modal">
            <div class="modal-content">
                <p>{{ modalMessage }}</p>
                <button @click="closeModal">OK</button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const url = ref('')
const showModal = ref(false)
const modalMessage = ref('')

function checkUrl() {
    if (url.value.startsWith('https://')) {
        window.location.href = url.value
    } else {
        modalMessage.value = 'Đường dẫn không hợp lệ'
        showModal.value = true
    }
}

function closeModal() {
    showModal.value = false
}
</script>

<style scoped>
.modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
}

.modal-content {
    background-color: #333;
    padding: 20px;
    border-radius: 5px;
    text-align: center;
    color: white;
}

button {
    background-color: #5fb6d8;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}
</style>