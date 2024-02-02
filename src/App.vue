<script setup>
import img from "./assets/images/img.jpg"
import Card from "@/components/Card.vue";
import Counter from "@/components/Counter.vue";

 const data = [
   { name: "Bart Simpson", age: 10, class: "fourth grade", img }
 ]
</script>

<template>
  <h1>Hello Vue</h1>
  <Counter />
</template>

<style>
ul, li {
    list-style: none;
  }

.btn {
  border-radius: 4px;
  width: 60px;
  height: 32px;
}
</style>
