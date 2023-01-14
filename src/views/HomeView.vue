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
    <div class="editCounter">
      <h3>Edit counter</h3>
      <input type="number" v-model="storeCounter.count">
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

.count {
  font-size: 48px;
  margin: 20px;
}

.buttons button {
  font-size: 24px;
  margin: 30px;
  width: 32px;
}

.oddOrEven {
  padding: 30px;
  border-top: thick double hsla(160, 100%, 37%, 1);
}

.editCounter {
  padding: 30px;
  border-top: thick solid hsla(160, 100%, 37%, 1);
}
</style>