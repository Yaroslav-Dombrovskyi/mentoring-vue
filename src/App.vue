<script setup>
import img from "./assets/images/img.jpg"
import Card from "@/components/Card.vue";

 const data = [
   { name: "Bart Simpson", age: 10, class: "fourth grade", img }
 ]
</script>

<template>
  <h1>Hello Vue</h1>
  <Card :data="data" />
</template>

<style scoped>
ul, li {
    list-style: none;
  }
</style>
