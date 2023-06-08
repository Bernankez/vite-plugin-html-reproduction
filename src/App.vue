<template>
  <div>
    <button @click="download">
      Download
    </button>
  </div>
</template>

<script setup lang="ts">
const download = () => {
  const formEl = document.createElement("form");
  formEl.style.display = "none";
  formEl.method = "GET";
  formEl.action = "/api/example.xlsx";
  const inputEl = document.createElement("input");
  inputEl.name = "example";
  inputEl.value = "exampleValue";
  formEl.appendChild(inputEl);
  document.body.appendChild(formEl);
  formEl.submit();
  document.body.removeChild(formEl);
};
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
