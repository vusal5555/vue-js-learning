<template>
  Username: {{ formData.username }} Email: {{ formData.email }} Password:
  {{ formData.password }}

  <form action="" class="form">
    <input
      type="text"
      placeholder="Enter Username"
      v-model="formData.username"
    />
    <input type="email" placeholder="Enter Email" v-model="formData.email" />
    <input
      type="password"
      placeholder="Enter Password"
      v-model="formData.password"
    />

    <button type="submit">Submit</button>
  </form>
</template>

<script setup>
import { ref } from "vue";

const formData = ref({ username: "", email: "", password: "" });
</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
}
</style>
