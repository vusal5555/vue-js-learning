<template>
  <!-- <p v-if="isTrue">isTrue is true</p>
  <p v-else-if="isFalse">isFalse is false</p>
  <p v-else>isTrue is false</p>

  <p v-show="isVisible">
    This paraghraph will be shown or hidden base on the value of isVisible
  </p>
  <button @click="isVisible = !isVisible">Toggle</button> -->

  <h1 v-if="isUserLoggedIn">Welcome {{ userName }}</h1>
  <p v-else>Please log in to access this content</p>

  <div v-show="userInfo">
    <h4>You are now able to modify your dashboard</h4>
  </div>

  <div v-if="isActive">
    <h1>My blog</h1>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maxime eos in
      fuga tempore possimus assumenda, excepturi sequi cumque adipisci
      voluptatibus, fugit dolore ipsa, amet officia? Nam atque nihil iure
      veritatis.
    </p>
  </div>

  <button @click="isActive = !isActive">Toggle Post</button>

  <h1 v-if="password.length > 8">Strong Password</h1>
  <h1 v-else-if="password.length < 8">Weak Password</h1>
  <h1 v-else>Please enter your password</h1>
</template>

<script setup>
import { ref } from "vue";
const isTrue = false;
const isFalse = true;

let isVisible = ref(true);
let isUserLoggedIn = ref(true);
let userName = "Vusal";
let userInfo = ref(isUserLoggedIn);
const isActive = ref(true);
let password = ref("mypersonalpassword");
</script>

<style scoped></style>
