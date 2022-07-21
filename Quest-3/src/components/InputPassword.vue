<script setup lang="ts">
import { createApp, ref } from "vue";
defineProps<{ msg: string }>();

const count = ref(0);

const switchVisibility = () => {
  const passwordField = document.getElementById("password");
  debugger;
  console.log(passwordField);
  if (passwordField.getAttribute("type") === "password")
    passwordField.setAttribute("type", "text");
  else passwordField.setAttribute("type", "password");
};
</script>

<template>
  <div>
    <input
      type="password"
      id="password"
    >
    <button @click="switchVisibility()">show / hide</button>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
