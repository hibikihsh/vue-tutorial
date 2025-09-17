<script setup>
import { ref } from "vue";

const message = ref("Reverse Message");

const reverseMessage = () => {
  message.value = message.value.split("").reverse().join("");
};

const appendExclamation = () => {
  message.value = message.value + "!";
};
</script>

<template>
  <h1>{{ message }}</h1>
  <button @click="reverseMessage">Reverse Message</button>
  <button @click="appendExclamation">Append '!'</button>
</template>
