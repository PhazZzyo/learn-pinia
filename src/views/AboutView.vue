<template>
  <div class="about">
    <h1>About</h1>
    <button class="counterButton" @click="storeCounter.increaseCount">{{ storeCounter.count }}</button>
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
  margin: 10px;
}
</style>