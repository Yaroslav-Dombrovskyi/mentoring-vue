<script setup>
import { computed, onMounted, ref } from "vue";
// no-reactive data
const title = "The Counter";
// reactive data
const count = ref(0);
const decrement = () => count.value -= 1;
const increment = () => count.value += 1;
// computed property
const countClass = computed(() => {
  if ( count.value > 3 ) {
    return "red"
  } else if ( count.value < 0 ) {
    return "blue"
  }
});
onMounted(() => console.log('hello from hook'));
</script>

<template>
  <div class="counter">
    <h2 class="count" :class="countClass">{{ count }}</h2>
    <div class="counter__actions">
      <button class="btn" @click="decrement">-</button>
      <button class="btn" @click="increment">+</button>
    </div>
  </div>
</template>

<style scoped>
.counter {
  padding: 20px;
}

.count {
  font-weight: 500;
  font-size: 26px;
}
.counter__actions {
  display: flex;
  gap: 10px;
}
.red {
  color: red;
}

.blue {
  color: blue;
}
</style>

