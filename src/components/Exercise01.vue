<template>
    <img :src="image" alt="">
    <div id="app" data-v-app>
        <h1 :id="elementId" :class="elementClass">Heading</h1>
    </div>

</template>

<script setup lang="ts">
import { ref } from 'vue'

const elementId = ref('heading')
const elementClass = ref('heading')
const image = "https://dthezntil550i.cloudfront.net/86/latest/861911302007288750002221253/05f85cab-dc3a-48e3-81ff-b7347d2e450b.png"
</script>

<style scoped>
img {
    height: 200px;
    width: 200px;
}
</style>