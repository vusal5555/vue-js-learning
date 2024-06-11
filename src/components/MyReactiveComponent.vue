<template>
  <h1>Count: {{ initialState.value.count }}</h1>
  <h2>{{ initialState.user }}</h2>

  <button @click="initialState.value.count = initialState.value.count + 10">
    Add 10
  </button>
  <button @click="changeUser()">Change User</button>
  <button @click="addUser('Vugar')">Add User</button>
</template>

<script setup>
import { reactive } from "vue";

let initialState = reactive({
  value: { count: 0 },
  user: ["Vusal", "Nurlan"],
});

console.log(initialState);

// const increment = () => {
//   initialState.count++;
// };
// const decrement = () => {
//   initialState.count--;
// };

const changeUser = () => {
  initialState.user[0] = "Kanan";
  initialState.user[1] = "Elvin";
};

const addUser = (user) => {
  initialState.user.push(user);
};
</script>

<style scoped></style>
