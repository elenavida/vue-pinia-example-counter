<script setup>
import { useCounterStore } from "../stores/counter";

const counterStore = useCounterStore();
</script>

<template>
  <main>
    {{ counterStore.counter }} x 2 = {{ counterStore.doubleCount }}
    <div class="buttons">
      <button @click="counterStore.decrement()">-</button>
      <button @click="counterStore.increment()">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  font-size: 80px;
  margin: 30px;
  text-align: center;
}
button {
  display: block;
  margin: 30px;
  width: 300px;
}
.buttons {
  display: flex;
  flex-direction: row;
}
</style>
