<template>
  <!-- <h1>Count: {{ count }}</h1>
  <h1>Username: {{ userName }}</h1>
  <h1>Userlist: {{ userList }}</h1>
  <button @click="count++">+</button>
  <button @click="count--">-</button>
  <button @click="userName = 'Vusal'">Change Name</button>
  <button @click="userList.push('Nurlan')">Add User</button> -->
  <h1>Name: {{ userInfo.name }}</h1>
  <h1>Age: {{ userInfo.age }}</h1>
  <h1>Location: {{ userInfo.location }}</h1>

  <h1 v-if="userInfo.isMarried">Married</h1>
  <h1 v-else>Not Married</h1>

  <button @click="userInfo.name = 'Kanan'">Change Name</button>
  <button @click="userInfo.age = 20">Change Age</button>
  <button @click="userInfo.location = ['Tbilisi', 'Georgia']">
    Change Age
  </button>
  <button @click="userInfo.isMarried = true">Change Marriage status</button>

  <h1>Friends {{ friends }}</h1>

  <button @click="friends[0] = 'Nurlan'">Change Friend</button>
</template>

<script setup>
import { reactive, ref } from "vue";

let count = ref(0);
let userName = ref("");
let userList = ref(["Micheal", "Jordan", "Vusal", "John"]);
let userInfo = ref({
  name: "Vusal",
  age: 22,
  location: ["Marneuli", "Georgia"],
  isMarried: false,
});

let friends = reactive([ref("Jordan"), ref("Alex"), ref("Vusal")]);
</script>

<style scoped></style>
