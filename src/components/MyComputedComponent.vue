<template>
  <h1>Count: {{ number }}</h1>
  <h1>SquaredCount: {{ squaredNumber }}</h1>
  <button @click="number++">Increment</button>
</template>

<script setup>
import { ref, computed } from "vue";

let number = ref(0);
const firstName = ref("Vusal");
const lastName = ref("Novruzov");

const fullName = computed(() => `${firstName.value} ${lastName.value}`);

const squaredNumber = computed(() => number.value ** 2);
</script>

<style scoped></style>
