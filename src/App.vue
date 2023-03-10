<script setup>
import { ref, nextTick } from 'vue';
const count = ref(0);

async function increment() {
  count.value++;

  console.log(document.getElementById('counter').textContent);

  await nextTick();

  console.log(document.getElementById('counter').textContent);
}
</script>

<template>
  <div>
    <button id="counter" @click="increment">{{ count }}</button>
  </div>
</template>

<style lang="scss" scoped>
body {
  button {
    font-size: 20px;
  }
}
</style>
