<script setup>
import { ref } from 'vue';

defineProps({
  label: String,
});

const count = ref(0);
</script>

<template>
  <div class="icon-wrapper">
    <div class="icon"></div>
    <div class="label">{{ label }}</div>
  </div>
</template>

<style scoped>
.icon-wrapper {
  padding-bottom: 1em;
  width: fit-content;
}
.icon {
  background: #c2e891;
  border-radius: 10px;
  box-shadow: 0px 1px 2px 1px rgba(0, 0, 0, 0.2);
  height: 60px;
  margin-bottom: 10px;
  width: 60px;
}
.label {
  font-family: sans-serif;
  font-size: 12px;
  text-align: center;
}
</style>
