<template>
  <div class="home">
    <h1>Home</h1>
    <Counter />
    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
    <div class="oddOrEven">
      <h2>This counter is: {{ storeCounter.oddOrEven }}</h2>
    </div>
  </div>
</template>

<script setup>
import Counter from '@/components/Counter.vue'
import { useCounterStore } from '@/stores/counter'
const storeCounter = useCounterStore()
</script>

<style>
.home {
  margin: 20px;
  text-align: center;
}

.buttons {
  border-top: thick double var(--color-border);
}

.buttons button {
  font-size: 24px;
  margin: 30px;
  width: 32px;
}

.oddOrEven {
  padding: 30px;
  text-decoration: underline;
}
</style>