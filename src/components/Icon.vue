<script setup>
defineProps({
  label: String,
});
</script>

<template>
  <div class="icon-wrapper">
    <img
      src="../assets/icon.png"
      srcset="../assets/icon.png, ../assets/icon@2x.png 2x"
      class="icon"
      :alt="label"
    />
    <div class="label">{{ label }}</div>
  </div>
</template>

<style scoped>
.icon-wrapper {
  cursor: grab;
  padding-bottom: 20px;
  width: fit-content;
}
.sortable-chosen {
  cursor: grabbing;
}
.icon {
  background: #c2e891;
  border-radius: 10px;
  box-shadow: 0px 1px 2px 1px rgba(0, 0, 0, 0.2);
  height: 80px;
  margin-bottom: 7px;
  width: 80px;
}
.label {
  font-family: sans-serif;
  font-size: 14px;
  text-align: center;
}
</style>
