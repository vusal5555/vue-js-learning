<template>
  <div>
    <h1>Count: {{ count }}</h1>
  </div>
  <button @click="increment()">Increment</button>
  <button @click="decrement()">Increment</button>

  <form @submit.prevent="onSubmit">
    <input type="text" placeholder="please enter your name" />
    <input type="text" placeholder="please enter your email" />
    <button type="submit">Submit</button>
  </form>
</template>

<script setup>
import { ref } from "vue";

let count = ref(0);

const increment = () => {
  count.value++;
};

const decrement = () => {
  count.value--;
};

const onSubmit = (e) => {
  alert("Valid credentials");
};
</script>

<style scoped></style>
