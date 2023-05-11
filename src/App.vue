<script setup>
import Icon from './components/Icon.vue';

const icons = [
  'Label 1',
  'Label 2',
  'Label 3',
  'Label 4',
  'Label 5',
  'Label 6',
];
</script>

<template>
  <div class="container">
    <Icon v-for="icon in icons" :label="icon" />
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  @media (min-width: 500px) {
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 30px 60px;
  }
  @media (min-width: 1000px) {
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    padding: 30px 60px;
  }
}
</style>
