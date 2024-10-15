<script setup lang="ts">
import Exercise01 from './components/Exercise01.vue';
import Exercise03 from './components/Exercise03.vue';
import Exercise04 from './components/Exercise04.vue';
import Exercise05 from './components/Exercise05.vue';
import Exercise06 from './components/Exercise06.vue';
import Exercise07 from './components/Exercise07.vue';

import { reactive, ref } from 'vue'
import Exercise08 from './components/Exercise08.vue';
import Exercise09 from './components/Exercise09.vue';

let test = ref(false)

function Changes(a: number) {
  console.log("da vao", a)
  test.value = !test.value
}

function EnterKey() {
  console.log("EnterKey")
}

const user = reactive({
  name: 'Gia Huy',
  age: 23,
});

const handleIncreaseAge = () => {
  user.age++
}

const index = ref(0)

const calculateFibonacci = (n:number) => {
  const fib = (n:number) => {
    if (n <= 1) return n
    return fib(n - 1) + fib(n - 2)
  }
  return fib(n)
}

const incrementIndex = () => {
  index.value++
}
</script>

<template>
  <Exercise01/>
  <Exercise03/>
  <Exercise04/>
  <Exercise05/>
  <Exercise06/>
  <Exercise07/>
  <Exercise08/>
  <Exercise09/>
  <h1 :class="test ? 'test':''">Hello</h1>
  <button v-on:click="Changes(5)">Change Color</button>
  <input @keydown.enter="EnterKey" type="text">
  <h3>Name: {{ user.name }}</h3>
  <h3>Age: {{ user.age }}</h3>
<button @click="handleIncreaseAge">Increase Age</button>
<div>
  <p>Fibonacci Index {{ index }}: {{ calculateFibonacci(index) }}</p>
  <button @click="incrementIndex">Increase Index</button>
</div>
</template>

<style scoped>
.test {
  color: red;
}
</style>
