<template>
  <div class="about">
    <h1>About</h1>
    <button class="counterButton" @click="storeCounter.increaseCount">{{ storeCounter.count }}</button>
    <div class="editCounter">
      <h3>Edit counter</h3>
      <input type="number" v-model="storeCounter.count">
    </div>
  </div>
</template>
<script setup>
import { useCounterStore } from '@/stores/counter'
const storeCounter = useCounterStore()
</script>

<style>
.about {
  margin: 20px;
  text-align: center;
}

.counterButton {
  font-size: 48px;
  margin: 30px;
}

.editCounter {
  padding: 30px;
  border-top: thick double var(--color-border);
}
</style>