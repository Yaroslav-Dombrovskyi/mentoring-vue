<script setup>
  const props = defineProps({
    data: {
      required: true,
      default: []
    }
  });
</script>

<template>
   <ul class="card__container">
     <li
         class="card__item"
         v-for="el in props.data"
         :key="el.id">
       <h2 class="card__title">{{el.name}}</h2>
       <img
           :src="el.img"
           alt="el.name"
           class="card__img"
       >
       <h4 class="card__age">Age: {{el.age}}</h4>
       <p class="card__description">Class: {{el.class}}</p>
     </li>
   </ul>
</template>

<style scoped>
  .card__container {
    padding: 12px 22px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
  }
  .card__title {
    font-size: 26px;
  }
  .card__img {
    border-radius: 4px;
    max-width: 260px;
  }
  .card__age {
    font-size: 22px;
    font-weight: 500;
  }
  .card__description {
    font-weight: 300;
  }
</style>