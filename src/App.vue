<script setup>
import { ref } from 'vue';
import draggable from 'vuedraggable';
import Icon from './components/Icon.vue';

const icons = ref([
  'Label 1',
  'Label 2',
  'Label 3',
  'Label 4',
  'Label 5',
  'Label 6',
]);
</script>

<template>
  <draggable class="container" v-model="icons" tag="div" :delay="500">
    <template #item="{ element: icon }">
      <Icon :label="icon" />
    </template>
  </draggable>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  place-items: center center;
  @media (min-width: 500px) {
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 20px 45px;
  }
  @media (min-width: 1000px) {
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    padding: 30px 60px;
  }
}
</style>
